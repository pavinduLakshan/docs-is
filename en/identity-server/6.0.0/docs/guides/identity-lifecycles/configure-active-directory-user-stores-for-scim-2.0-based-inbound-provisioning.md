# Configure Active Directory Userstores for SCIM 2.0 based Inbound Provisioning

WSO2 Identity Server can act both as a SCIM Provider and a SCIM consumer at the same time. You can test the WSO2 Identity Server's SCIM 2.0 Provider API as described here.

When the WSO2 Identity Server is connected to an Active Directory instance, they might not have these mandatory SCIM attributes in their schema. So the option is to map the SCIM claims to the existing attributes of the Active Directory.

Add a user with the username "Alex" and password "Wso2@123". Here we have to map the **userName** (urn:ietf:params:scim:schemas:core:2.0:User) SCIM attribute to an existing claim in the Active Directory (e.g.: cn).

Furthermore, when a user is being added using SCIM, four more SCIM attributes are being added behind the scenes including:

- **location** (`urn:ietf:params:scim:schemas:core:2.0`),
- **created** (`urn:ietf:params:scim:schemas:core:2.0`),
- **lastModified** (`urn:ietf:params:scim:schemas:core:2.0`)
- **id** (`urn:ietf:params:scim:schemas:core:2.0`)

These attributes need to be mapped to the existing Active Directory user attributes as well.

The SCIM claim dialect (`urn:ietf:params:scim:schemas:core:2.0:User` and `urn:ietf:params:scim:schemas:core:2.0`) uses `String` type to hold their values. So, when mapping any SCIM claim to an attribute in the Active Directory, make sure to use the attributes of `String` type. You can find all Active Directory attributes [here](https://docs.microsoft.com/en-us/windows/win32/adschema/attributes-all).

When a user or a group is created with SCIM 2.0, there is a set of mandatory SCIM 2.0 claim values that need to be saved along with the user or group. Some of these values are as follows.

- urn:ietf:params:scim:schemas:core:2.0:meta.location
- urn:ietf:params:scim:schemas:core:2.0:meta.resourceType
- urn:ietf:params:scim:schemas:core:2.0:meta.version
- urn:ietf:params:scim:schemas:core:2.0:meta.created
- urn:ietf:params:scim:schemas:core:2.0:id
- urn:ietf:params:scim:schemas:core:2.0:meta.lastModified
- urn:ietf:params:scim:schemas:core:2.0:User:userName

This claim mapping can be done through the WSO2 Identity Server Claim Management Feature.

## Step 1: Set up the secondary user store

You need to configure the secondary user store. This can be done in the following methods:

- [Using the management console]({{base_path}}/deploy/configure-secondary-user-stores/#configure-using-the-management-console)

    For this use case, you can select any one of the following **Userstore Manager Class** from the list:

    - `org.wso2.carbon.user.core.ldap.ActiveDirectoryUserStoreManager` <sup><b>RECOMMENDED</b></sup>
    - `org.wso2.carbon.user.core.ldap.UniqueIDActiveDirectoryUserStoreManager`

- [Manually]({{base_path}}/deploy/configure-secondary-user-stores/#configure-manually)

    If you are using `org.wso2.carbon.user.core.ldap.ActiveDirectoryUserStoreManager` class to configure the user store, use the following user store file configuration.

    ??? note "User store file configuration"
        ```xml
        <?xml version=”1.0" encoding=”UTF-8"?><UserStoreManager class=”org.wso2.carbon.user.core.ldap.ActiveDirectoryUserStoreManager”>
        <Property name=”ConnectionURL”>***************</Property>
        <Property name=”ConnectionName”>CN=ADMIN,CN=Users,DC=abc,DC=abcd</Property>
        <Property name=”ConnectionPassword”>*************</Property>
        <Property name=”UserSearchBase”>CN=Users,DC=abc,DC=abcd</Property>
        <Property name=”UserEntryObjectClass”>user</Property>
        <Property name=”UserNameAttribute”>cn</Property>
        <Property name=”UserNameSearchFilter”>(&amp;(objectClass=user)(cn=?))</Property>
        <Property name=”UserNameListFilter”>(objectClass=user)</Property>
        <Property name=”UserDNPattern”/>
        <Property name=”DisplayNameAttribute”/>
        <Property name=”Disabled”>false</Property>
        <Property name=”ReadGroups”>true</Property>
        <Property name=”WriteGroups”>true</Property>
        <Property name=”GroupSearchBase”>CN=Users,DC=abc,DC=abcd</Property>
        <Property name=”GroupEntryObjectClass”>group</Property>
        <Property name=”GroupNameAttribute”>cn</Property>
        <Property name=”GroupNameSearchFilter”>(&amp;(objectClass=group)(cn=?))</Property>
        <Property name=”GroupNameListFilter”>(objectcategory=group)</Property>
        <Property name=”RoleDNPattern”/>
        <Property name=”MembershipAttribute”>member</Property>
        <Property name=”MemberOfAttribute”>memberOf</Property>
        <Property name=”BackLinksEnabled”>true</Property>
        <Property name=”Referral”>follow</Property>
        <Property name=”UserNameJavaRegEx”>[a-zA-Z0–9._-|//]{3,30}$</Property>
        <Property name=”UserNameJavaScriptRegEx”>^[\S]{3,30}$</Property>
        <Property name=”UsernameJavaRegExViolationErrorMsg”>Username pattern policy violated.</Property>
        <Property name=”PasswordJavaRegEx”>^[\S]{5,30}$</Property>
        <Property name=”PasswordJavaScriptRegEx”>^[\S]{5,30}$</Property>
        <Property name=”PasswordJavaRegExViolationErrorMsg”>Password pattern policy violated.</Property>
        <Property name=”RoleNameJavaRegEx”>^[a-zA-Z0–9._-|//]{3,30}$</Property>
        <Property name=”RoleNameJavaScriptRegEx”>^[\S]{3,30}$</Property>
        <Property name=”BulkImportSupported”>true</Property>
        <Property name=”EmptyRolesAllowed”>true</Property>
        <Property name=”PasswordHashMethod”>PLAIN_TEXT</Property>
        <Property name=”MultiAttributeSeparator”>,</Property>
        <Property name=”isADLDSRole”>false</Property>
        <Property name=”userAccountControl”>512</Property>
        <Property name=”MaxUserNameListLength”>100</Property>
        <Property name=”MaxRoleNameListLength”>100</Property>
        <Property name=”kdcEnabled”>false</Property>
        <Property name=”defaultRealmName”>WSO2.ORG</Property>
        <Property name=”UserRolesCacheEnabled”>true</Property>
        <Property name=”ConnectionPoolingEnabled”>false</Property>
        <Property name=”LDAPConnectionTimeout”>5000</Property>
        <Property name=”ReadTimeout”>5000</Property>
        <Property name=”RetryAttempts”>0</Property>
        <Property name=”CountRetrieverClass”/>
        <Property name=”java.naming.ldap.attributes.binary”>objectGuid</Property>
        <Property name=”ClaimOperationsSupported”>true</Property>
        <Property name=”transformObjectGUIDToUUID”>true</Property>
        <Property name=”MembershipAttributeRange”>1500</Property>
        <Property name=”UserCacheExpiryMilliseconds”/>
        <Property name=”UserDNCacheEnabled”>true</Property>
        <Property name=”StartTLSEnabled”>false</Property>
        <Property name=”EnableMaxUserLimitForSCIM”>false</Property>
        <Property name=”ImmutableAttributes”>objectGuid,whenCreated,whenChanged</Property>
        <Property name=”TimestampAttributes”>whenChanged,whenCreated</Property>
        <Property name=”DomainName”>abc</Property>
        <Property name=”Description”/>
        </UserStoreManager>

        Use below user store configurations if you are using the UniqueIDActiveDirectoryUserStoreManager.

        <?xml version=”1.0" encoding=”UTF-8"?><UserStoreManager class=”org.wso2.carbon.user.core.ldap.UniqueIDActiveDirectoryUserStoreManager”>
        <Property name=”ConnectionURL”>***************</Property>
        <Property name=”ConnectionName”>CN=ADMIN,CN=Users,DC=abc,DC=abcd</Property>
        <Property name=”ConnectionPassword”>*************</Property>
        <Property name=”UserSearchBase”>CN=Users,DC=abc,DC=abcd</Property>
        <Property name=”UserEntryObjectClass”>user</Property>
        <Property name=”UserNameAttribute”>cn</Property>

        <Property name=”UserIDAttribute”>objectGuid</Property>

        <Property name=”UserIdSearchFilter”>(&amp;(objectClass=user)(objectGuid=?))</Property>
        <Property name=”UserNameSearchFilter”>(&amp;(objectClass=user)(cn=?))</Property>
        <Property name=”UserNameListFilter”>(objectClass=user)</Property>
        <Property name=”UserDNPattern”/>
        <Property name=”DisplayNameAttribute”/>
        <Property name=”Disabled”>false</Property>
        <Property name=”ReadGroups”>true</Property>
        <Property name=”WriteGroups”>true</Property>
        <Property name=”GroupSearchBase”>CN=Users,DC=abc,DC=abcd</Property>
        <Property name=”GroupEntryObjectClass”>group</Property>
        <Property name=”GroupNameAttribute”>cn</Property>
        <Property name=”GroupNameSearchFilter”>(&amp;(objectClass=group)(cn=?))</Property>
        <Property name=”GroupNameListFilter”>(objectcategory=group)</Property>
        <Property name=”RoleDNPattern”/>
        <Property name=”MembershipAttribute”>member</Property>
        <Property name=”MemberOfAttribute”>memberOf</Property>
        <Property name=”BackLinksEnabled”>true</Property>
        <Property name=”Referral”>follow</Property>
        <Property name=”UserNameJavaRegEx”>[a-zA-Z0–9._-|//]{3,30}$</Property>
        <Property name=”UserNameJavaScriptRegEx”>^[\S]{3,30}$</Property>
        <Property name=”UsernameJavaRegExViolationErrorMsg”>Username pattern policy violated.</Property>
        <Property name=”PasswordJavaRegEx”>^[\S]{5,30}$</Property>
        <Property name=”PasswordJavaScriptRegEx”>^[\S]{5,30}$</Property>
        <Property name=”PasswordJavaRegExViolationErrorMsg”>Password pattern policy violated.</Property>
        <Property name=”RoleNameJavaRegEx”>^[a-zA-Z0–9._-|//]{3,30}$</Property>
        <Property name=”RoleNameJavaScriptRegEx”>^[\S]{3,30}$</Property>
        <Property name=”BulkImportSupported”>true</Property>
        <Property name=”EmptyRolesAllowed”>true</Property>
        <Property name=”PasswordHashMethod”>PLAIN_TEXT</Property>
        <Property name=”MultiAttributeSeparator”>,</Property>
        <Property name=”isADLDSRole”>false</Property>
        <Property name=”userAccountControl”>512</Property>
        <Property name=”MaxUserNameListLength”>100</Property>
        <Property name=”MaxRoleNameListLength”>100</Property>
        <Property name=”kdcEnabled”>false</Property>
        <Property name=”defaultRealmName”>WSO2.ORG</Property>
        <Property name=”UserRolesCacheEnabled”>true</Property>
        <Property name=”ConnectionPoolingEnabled”>false</Property>
        <Property name=”LDAPConnectionTimeout”>5000</Property>
        <Property name=”ReadTimeout”>5000</Property>
        <Property name=”RetryAttempts”>0</Property>
        <Property name=”CountRetrieverClass”/>
        <Property name=”java.naming.ldap.attributes.binary”>objectGuid</Property>
        <Property name=”ClaimOperationsSupported”>true</Property>
        <Property name=”transformObjectGUIDToUUID”>true</Property>
        <Property name=”MembershipAttributeRange”>1500</Property>
        <Property name=”UserCacheExpiryMilliseconds”/>
        <Property name=”UserDNCacheEnabled”>true</Property>
        <Property name=”StartTLSEnabled”>false</Property>
        <Property name=”EnableMaxUserLimitForSCIM”>false</Property>
        <Property name=”ImmutableAttributes”>objectGuid,whenCreated,whenChanged</Property>
        <Property name=”TimestampAttributes”>whenChanged,whenCreated</Property>
        <Property name=”DomainName”>abc</Property>
        <Property name=”Description”/>
        </UserStoreManager>
        ```

## Step 2: Import the user store certificate

To import the user store certificate to the WSO2 Identity Server trust store, navigate to `<IS_HOME>repository/resources/security` folder and execute the following command:

``` shell
keytool -import -alias certalias -file <certificate>.pem -keystore client-truststore.jks -storepass wso2carbon
```

## Step 3: Map WSO2 claims to AD attribute

Following are the mandatory basic claim mappings that need to be done and this will be extended as per your requirements.

| Local Claim   | Mapped Attribute  |
|---------------|-------------------|
| `http://wso2.org/claims/location` | streetAddress |
| `http://wso2.org/claims/resourceType` | unixHomeDirectory |
| `http://wso2.org/claims/im` | userWorkstations |
| `http://wso2.org/claims/created` | whenCreated |
| `http://wso2.org/claims/userid` | objectGuid |
| `http://wso2.org/claims/modified` | whenChanged |
| `http://wso2.org/claims/username` | cn |

To configure the claim mappings:

1. On the Management Console, go to **Identity** > **Claims** and click **List**.
2. Select `http://wso2.org/claims` from the list.
3. Choose one of the above-mentioned mandatory local claims.
4. Enter the **Mapped Attribute (s)** as specified in the table above and click **Update** to save the configurations.
5. Repeat steps three and four for the remaining mandatory local claims.

Learn more on [how to configure claim mappings]({{base_path}}/guides/dialects/edit-claim-mapping/).


## Step 4: Configure additional properties

This step of the guide helps to categorize the types of attributes used in Active Directory on the WSO2 Identity Server.

Categorizing the attributes makes it easier to perform the necessary conversions when communicating between the AD and the WSO2 Identity Server.

### Timestamp attribute

The Active directory attributes `whenChanged` and `whenCreated` should be added as a timestamp attribute. In AD, timestamp values are stored in a generalized time format. Therefore reading time values from AD and passing these values to WSO2IS requires a time conversion to UTC format.

You can configure these timestamp attributes using the following methods:

- Using the Management console:

    1. On the Management console, go to **Userstores** > **List**
    2. Click **Edit** corresponding to your secondary user store.
    3. Expand **Advanced** and add `whenChanged,whenCreated` as **Timestamp Attributes**.
    4. Click **Update** to save the configurations.

- Manually updating the configuration file:

    Add the following configuration to the `<userstore>.xml` file in the `<IS_HOME>/repository/deployment/server/userstores` folder:

    ``` xml
    <Property name=”TimestampAttributes”>whenChanged,whenCreated</Property>
    ```

### Immutable attributes

The Active Directory attributes, `objectGuid`, `whenCreated`, and `whenChanged` are immutable, meaning that they cannot be changed.

You can configure the immutable attributes using the following methods:

- Using the Management console:

    1. On the Management console, go to **Userstores** > **List**
    2. Click **Edit** corresponding to your secondary user store.
    3. Expand **Advanced** and add `objectGuid,whenChanged,whenCreated` as **Immutable Attributes**.
    4. Click **Update** to save the configurations.

- Manually updating the configuration file:

    Add the following configuration to the `<userstore>.xml` file in the `<IS_HOME>/repository/deployment/server/userstores` folder:

    ``` xml
    <Property name=”ImmutableAttributes”>objectGuid,whenCreated,whenChanged</Property>
    ```

### ObjectGUID attribute

The `objectGUID` attribute serves as the immutable identifier within Active Directory and is widely utilized as the primary identifier for many applications. In certain scenarios, you may find it necessary to leverage the `objectGUID` attribute as a distinct and unique attribute. This attribute can then be mapped into a local claim within the WSO2 Identity Server.

To do this you need to [add objectGUID under immutableAttributes](#immutable-attributes) and configure the LDAP binary attributes using the following methods:

- Using the Management console:

    1. On the Management console, go to **Userstores** > **List**
    2. Click **Edit** corresponding to your secondary user store.
    3. Expand **Advanced**, select **Return objectGUID in UUID Canonical Format** and add `objectGuid` as **LDAP binary attributes**
    4. Click **Update** to save the configurations.

- Manually updating the configuration file:

    Add the following configuration to the `<userstore>.xml` file in the `<IS_HOME>/repository/deployment/server/userstores` folder:

    ``` xml
    <Property name=”transformObjectGUIDToUUID”>true</Property>

    <Property name=”java.naming.ldap.attributes.binary”>objectGuid</Property>
    ```

## Step 5: Accessing the APIs

Now the basic claim mapping is done. You can now add a user using the curl commands [here]({{base_path}}/apis/scim2-rest-apis).

In RestClient, the following header parameters must be added and the double quotations must be removed from the message body.

```
Content-Type: application/json
Accept: */*
Message body
{schemas:[],userName:'wso2.com/uresh67',password:Wso2@123}
```

!!! info
    You need to do the claim mapping for every SCIM claim you are using with user operations.

!!! info "Related topics"
    - [Concepts: Provisioning Framework]({{base_path}}/references/concepts/provisioning-framework/#inbound-provisioning)