# API Permissions

The following table lists out all the available APIs and their
operations and specifies the permissions of each operation.

<table>
<thead>
<tr class="header">
<th>Service</th>
<th>Operation</th>
<th>Permission Level</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>IdentityProviderMgtService</strong></td>
<td>addIdP</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>deleteIdP</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getAllFederatedAuthenticators</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAllIdPs</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getAllLocalClaimUris</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAllProvisioningConnectors</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getEnabledAllIdPs</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getIdPByName</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getResidentIdP</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>updateIdP</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>updateResidentIdP</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="even">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="odd">
<td><strong>IdentityApplicationManagementService</strong></td>
<td>createApplication</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>deleteApplication</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getAllApplicationBasicInfo</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAllIdentityProviders</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getAllLocalAuthenticators</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAllLocalClaimUris</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getAllRequestPathAuthenticators</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getApplication</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getIdentityProvider</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>updateApplication</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="even">
<td><strong>TenantMgtAdminService</strong></td>
<td>activateTenant</td>
<td>/permission/protected/manage/modify/tenants</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>addSkeletonTenant</td>
<td>/permission/protected/manage/monitor/tenants</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>addTenant</td>
<td>/permission/protected/manage/monitor/tenants</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>deactivateTenant</td>
<td>/permission/protected/manage/modify/tenants</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>deleteTenant</td>
<td>/permission/protected/manage/modify/tenants</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getTenant</td>
<td>/permission/protected/manage/monitor/tenants</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>retrievePaginatedPartialSearchTenants</td>
<td>/permission/protected/manage/monitor/tenants</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>retrievePaginatedTenants</td>
<td>/permission/protected/manage/monitor/tenants</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>retrievePartialSearchTenants</td>
<td>/permission/protected/manage/monitor/tenants</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>retrieveTenants</td>
<td>/permission/protected/manage/monitor/tenants</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>updateTenant</td>
<td>/permission/protected/manage/modify/tenants</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="even">
<td><strong>UserStoreConfigAdminService</strong></td>
<td>addUserStore</td>
<td>/permission/admin/manage/identity/userstore/config/create</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>changeUserStoreState</td>
<td>/permission/admin/manage/identity/userstore/config/update</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>deleteUserStore</td>
<td>/permission/admin/manage/identity/userstore/config/delete</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>deleteUserStoresSet</td>
<td>/permission/admin/manage/identity/userstore/config/delete</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>editUserStore</td>
<td>/permission/admin/manage/identity/userstore/config/update</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>editUserStoreWithDomainName</td>
<td>/permission/admin/manage/identity/userstore/config/update</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAvailableUserStoreClasses</td>
<td>/permission/admin/manage/identity/userstore/config/view</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getSecondaryRealmConfigurations</td>
<td>/permission/admin/manage/identity/userstore/config/view</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getUserStoreManagerProperties</td>
<td>/permission/admin/manage/identity/userstore/config/view</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>testRDBMSConnection</td>
<td>/permission/admin/manage/identity/userstore/config/view</td>
</tr>
<tr class="even">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="odd">
<td><strong>OAuthAdminService</strong></td>
<td>getAllOAuthApplicationData</td>
<td>/permission/admin/manage/identity/applicationmgt/view</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAllowedGrantTypes</td>
<td>/permission/admin/manage/identity/applicationmgt/view</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getAppsAuthorizedByUser</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getOAuthApplicationData</td>
<td>/permission/admin/manage/identity/applicationmgt/view</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getOAuthApplicationDataByAppName</td>
<td>/permission/admin/manage/identity/applicationmgt/view</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>registerOAuthApplicationData</td>
<td>/permission/admin/manage/identity/applicationmgt/create</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>registerOAuthConsumer</td>
<td>/permission/admin/manage/identity/applicationmgt/create</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>removeOAuthApplicationData</td>
<td>/permission/admin/manage/identity/applicationmgt/delete</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>revokeAuthzForAppsByResoureOwner</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>updateConsumerApplication</td>
<td>/permission/admin/manage/identity/applicationmgt/update</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="even">
<td><strong>OAuth2TokenValidationService</strong></td>
<td>findOAuthConsumerIfTokenIsValid</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>validate</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="even">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="odd">
<td><strong>ClaimManagementService</strong></td>
<td>addNewClaimDialect</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>addNewClaimMapping</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getClaimMappingByDialect</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getClaimMappings</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>removeClaimDialect</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>removeClaimMapping</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>upateClaimMapping</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="odd">
<td><strong>RemoteUserStoreManagerService</strong></td>
<td>addRole</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>addUser</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>addUserClaimValue</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>addUserClaimValues</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>authenticate</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>deleteRole</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>deleteUser</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>deleteUserClaimValue</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>deleteUserClaimValues</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAllProfileNames</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getHybridRoles</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getPasswordExpirationTime</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getProfileNames</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getProperties</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getRoleListOfUser</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getRoleNames</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getTenantId</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getTenantIdofUser</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getUserClaimValue</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getUserClaimValues</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getUserClaimValuesForClaims</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getUserId</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getUserList</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getUserListOfRole</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>isExistingRole</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>isExistingUser</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>isReadOnly</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>listUsers</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>setUserClaimValue</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>setUserClaimValues</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>updateCredential</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>updateCredentialByAdmin</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>updateRoleListOfUser</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>updateRoleName</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>updateUserListOfRole</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="odd">
<td><strong>RemoteAuthorizationManagerService</strong></td>
<td>authorizeRole</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>authorizeUser</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>clearAllRoleAuthorization</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>clearAllUserAuthorization</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>clearResourceAuthorizations</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>clearRoleActionOnAllResources</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>clearRoleAuthorization</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>clearUserAuthorization</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>denyRole</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>denyUser</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getAllowedRolesForResource</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAllowedUIResourcesForUser</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getDeniedRolesForResource</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getExplicitlyAllowedUsersForResource</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getExplicitlyDeniedUsersForResource</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>isRoleAuthorized</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>isUserAuthorized</td>
<td>/permission/admin/manage/identity</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>resetPermissionOnUpdateRole</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="even">
<td><strong>RemoteProfileConfigurationManagerService</strong></td>
<td>addProfileConfig</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>deleteProfileConfig</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAllProfiles</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getProfileConfig</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>updateProfileConfig</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="even">
<td><strong>RemoteClaimManagerService</strong></td>
<td>addNewClaimMapping</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>deleteClaimMapping</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAllClaimMappings</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getAllClaimUris</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAllRequiredClaimMappings</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getAllSupportClaimMappingsByDefault</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAttributeName</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getAttributeNameFromDomain</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getClaim</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getClaimMapping</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>updateClaimMapping</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="even">
<td><strong>RemoteUserRealmService</strong></td>
<td>getRealmConfiguration</td>
<td>/permission/protected/tenant-admin</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="even">
<td><strong>RemoteTenantManagerService</strong></td>
<td>activateTenant</td>
<td>/permission/protected/tenant-admin</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>addTenant</td>
<td>/permission/protected/tenant-admin</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>deactivateTenant</td>
<td>/permission/protected/tenant-admin</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>deleteTenant</td>
<td>/permission/protected/tenant-admin</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAllTenants</td>
<td>/permission/protected/tenant-admin</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getDomain</td>
<td>/permission/protected/tenant-admin</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getSuperTenantDomain</td>
<td>/permission/protected/tenant-admin</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getTenant</td>
<td>/permission/protected/tenant-admin</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getTenantId</td>
<td>/permission/protected/tenant-admin</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>isTenantActive</td>
<td>/permission/protected/tenant-admin</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>updateTenant</td>
<td>/permission/protected/tenant-admin</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="even">
<td><strong>UserIdentityManagementAdminService</strong></td>
<td>changeUserPassword</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>deleteUser</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAllChallengeQuestions</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getAllPromotedUserChallenge</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAllUserIdentityClaims</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getChallengeQuestionsOfUser</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>isReadOnlyUserStore</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>lockUserAccount</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>resetUserPassword</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>setChallengeQuestions</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>setChallengeQuestionsOfUser</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>unlockUserAccount</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>updateUserIdentityClaims</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="even">
<td><strong>AccountCredentialMgtConfigService</strong></td>
<td>getEmailConfig</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>saveEmailConfig</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="odd">
<td><strong>UserInformationRecoveryService</strong></td>
<td>confirmUserSelfRegistration</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAllChallengeQuestions</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getCaptcha</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getUserChallengeQuestion</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getUserChallengeQuestionIds</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getUserIdentitySupportedClaims</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>registerUser</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>sendRecoveryNotification</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>updatePassword</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>verifyAccount</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>verifyConfirmationCode</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>verifyUser</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>verifyUserChallengeAnswer</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="odd">
<td><strong>EntitlementAdminService</strong></td>
<td>clearAllAttributeCaches</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>clearAllResourceCaches</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>clearAttributeFinderCache</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>clearAttributeFinderCacheByAttributes</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>clearCarbonAttributeCache</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>clearCarbonResourceCache</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>clearDecisionCache</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>clearPolicyCache</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>clearResourceFinderCache</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>doTestRequest</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>doTestRequestForGivenPolicies</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getGlobalPolicyAlgorithm</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getPDPData</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getPIPAttributeFinderData</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getPIPResourceFinderData</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getPolicyFinderData</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>refreshAttributeFinder</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>refreshPolicyFinders</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>refreshResourceFinder</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>setGlobalPolicyAlgorithm</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="even">
<td><strong>EntitlementPolicyAdminService</strong></td>
<td>addPolicies</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>addPolicy</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>addSubscriber</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>deleteSubscriber</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>dePromotePolicy</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>enableDisablePolicy</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAllPolicies</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getAllPolicyIds</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getEntitlementData</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getEntitlementDataModules</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getLightPolicy</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getPolicy</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getPolicyByVersion</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getPolicyVersions</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getPublisherModuleData</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getStatusData</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getSubscriber</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getSubscriberIds</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>importPolicyFromRegistry</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>orderPolicy</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>publish</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>publishPolicies</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>publishToPDP</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>removePolicies</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>removePolicy</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>rollBackPolicy</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>updatePolicy</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>updateSubscriber</td>
<td>/permission/admin/configure</td>
</tr>
<tr class="even">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="odd">
<td><strong>EntitlementService</strong></td>
<td>getAllEntitlements</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getBooleanDecision</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getDecision</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getDecisionByAttributes</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getEntitledAttributes</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>XACMLAuthzDecisionQuery</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="even">
<td>ws-xacml</td>
<td>XACMLAuthzDecisionQuery</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="even">
<td><strong>UserProfileMgtService</strong></td>
<td>associateID</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>deleteUserProfile</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAssociatedIDs</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getInstance</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getNameAssociatedWith</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getProfileFieldsForInternalStore</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getUserProfile</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getUserProfiles</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>isAddProfileEnabled</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>isAddProfileEnabledForDomain</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>isReadOnlyUserStore</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>removeAssociateID</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>setUserProfile</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="even">
<td><strong>UserAdmin</strong></td>
<td>addInternalRole</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>addRemoveRolesOfUser</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>addRemoveUsersOfRole</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>addRole</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>addUser</td>
<td>/permission/admin/configure/security/usermgt/users</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>bulkImportUsers</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>changePassword</td>
<td>/permission/admin/configure/security/usermgt/passwords</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>changePasswordByUser</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>deleteRole</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>deleteUser</td>
<td>/permission/admin/configure/security/usermgt/users</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAllRolesNames</td>
<td>/permission/admin/configure/security/rolemgt,/permission/admin/manage/modify/service</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getAllSharedRoleNames</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAllUIPermissions</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getRolePermissions</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getRolesOfCurrentUser</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getRolesOfUser</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getUserRealmInfo</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getUsersOfRole</td>
<td>/permission/admin/configure/security/rolemgt</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>hasMultipleUserStores</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>isSharedRolesEnabled</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>listAllUsers</td>
<td>/permission/admin/configure/security/usermgt/users,/permission/admin/configure/security/usermgt/passwords,/permission/admin/configure/security/usermgt/profiles</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>listUserByClaim</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>listUsers</td>
<td>/permission/admin/configure/security/usermgt/users,/permission/admin/configure/security/usermgt/passwords,/permission/admin/configure/security/usermgt/profiles</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>setRoleUIPermission</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>updateRoleName</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>updateRolesOfUser</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>updateUsersOfRole</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="even">
<td><strong>MultipleCredentialsUserAdmin</strong></td>
<td>addCredential</td>
<td>/permission/admin/configure/security/usermgt/passwords</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>addUser</td>
<td>/permission/admin/configure/security/usermgt/users</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>addUsers</td>
<td>/permission/admin/configure/security/usermgt/users</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>addUserWithUserId</td>
<td>/permission/admin/configure/security/usermgt</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>authenticate</td>
<td>/permission/admin/configure/security/usermgt</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>deleteCredential</td>
<td>/permission/admin/configure/security/usermgt/passwords</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>deleteUser</td>
<td>/permission/admin/configure/security/usermgt/users</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>deleteUserClaimValue</td>
<td>/permission/admin/configure/security/usermgt</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>deleteUserClaimValues</td>
<td>/permission/admin/configure/security/usermgt</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getAllUserClaimValues</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getCredentials</td>
<td>/permission/admin/configure/security/usermgt/passwords</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getUserClaimValue</td>
<td>/permission/admin/configure/security/usermgt</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getUserClaimValues</td>
<td>/permission/admin/configure/security/usermgt</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getUserId</td>
<td>/permission/admin/configure/security/usermgt</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>setUserClaimValue</td>
<td>/permission/admin/configure/security/usermgt</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>setUserClaimValues</td>
<td>/permission/admin/configure/security/usermgt</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>updateCredential</td>
<td>/permission/admin/configure/security/usermgt/passwords</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="even">
<td><strong>IdentityProviderAdminService</strong></td>
<td>addOpenID</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>extractPrimaryUserName</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAllOpenIDs</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getPrimaryOpenID</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>removeOpenID</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="even">
<td><strong>XMPPConfigurationService</strong></td>
<td>addUserXmppSettings</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>editXmppSettings</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getUserIM</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getXmppSettings</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>hasXMPPSettings</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>isXMPPSettingsEnabled</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="odd">
<td><strong>IdentitySAMLSSOConfigService</strong></td>
<td>addRPServiceProvider</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getCertAliasOfPrimaryKeyStore</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getClaimURIs</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getServiceProviders</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>removeServiceProvider</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="even">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="odd">
<td><strong>IdentitySTSAdminService</strong></td>
<td>readCardIssuerConfiguration</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>updateCardIssueConfiguration</td>
<td>/permission/admin/manage</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="even">
<td><strong>IWAAuthenticator</strong></td>
<td>canHandle</td>
<td>/permission/admin/login</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>login</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="odd">
<td><strong>ProvisioningAdminService</strong></td>
<td>getAllInstalledFeatures</td>
<td>/permission/protected/configure/components</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getInstalledFeatureInfo</td>
<td>/permission/protected/configure/components</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getInstalledFeaturesWithProperty</td>
<td>/permission/protected/configure/components</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getLicensingInformation</td>
<td>/permission/protected/configure/components</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getProfileHistory</td>
<td>/permission/protected/configure/components</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>performProvisioningAction</td>
<td>/permission/protected/configure/components</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>removeAllConsoleFeatures</td>
<td>/permission/protected/configure/components</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>removeAllServerFeatures</td>
<td>/permission/protected/configure/components</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>reviewProvisioningAction</td>
<td>/permission/protected/configure/components</td>
</tr>
<tr class="even">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="odd">
<td><strong>ProfilesAdminService</strong></td>
<td>getUserProfile</td>
<td>/permission/admin/manage/modify/user-profile</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>putUserProfile</td>
<td>/permission/admin/manage/modify/user-profile</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="even">
<td><strong>SecurityAdminService</strong></td>
<td>activateUsernameTokenAuthentication</td>
<td>/permission/admin/manage/modify/service</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>applyKerberosSecurityPolicy</td>
<td>/permission/admin/manage/modify/service</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>applySecurity</td>
<td>/permission/admin/manage/modify/service</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>disableSecurityOnService</td>
<td>/permission/admin/manage/modify/service</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getScenarios</td>
<td>/permission/admin/manage/modify/service</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getSecurityConfigData</td>
<td>/permission/admin/manage/modify/service</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getSecurityScenario</td>
<td>/permission/admin/manage/modify/service</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="even">
<td><strong>STSAdminService</strong></td>
<td>addTrustedService</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getCertAliasOfPrimaryKeyStore</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getProofKeyType</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getTrustedServices</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>removeTrustedService</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>setProofKeyType</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="odd">
<td><strong>KeyStoreAdminService</strong></td>
<td>addKeyStore</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>addTrustStore</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>deleteStore</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getKeystoreInfo</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getKeyStores</td>
<td>/permission/admin/configure/security,/permission/admin/manage/modify/service</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getPaginatedKeystoreInfo</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getStoreEntries</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>importCertToStore</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>removeCertFromStore</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="odd">
<td><strong>SCIMConfigAdminService</strong></td>
<td>addGlobalProvider</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>addUserProvider</td>
<td>/permission/admin/configure/security/usermgt/provisioning</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>deleteGlobalProvider</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>deleteUserProvider</td>
<td>/permission/admin/configure/security/usermgt/provisioning</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getAllGlobalProviders</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAllUserProviders</td>
<td>/permission/admin/configure/security/usermgt/provisioning</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getGlobalProvider</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getUserProvider</td>
<td>/permission/admin/configure/security/usermgt/provisioning</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>updateGlobalProvider</td>
<td>/permission/admin/configure/security</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>updateUserProvider</td>
<td>/permission/admin/configure/security/usermgt/provisioning</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="even">
<td><strong>DirectoryServerManager</strong></td>
<td>addServer</td>
<td>/permission/admin/configure/security,/permission/admin/manage/modify/service</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>changePassword</td>
<td>/permission/admin/configure/security,/permission/admin/manage/modify/service</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getPasswordConformanceRegularExpression</td>
<td>/permission/admin/configure/security,/permission/admin/manage/modify/service</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getServiceNameConformanceRegularExpression</td>
<td>/permission/admin/configure/security,/permission/admin/manage/modify/service</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>isExistingServicePrinciple</td>
<td>/permission/admin/configure/security,/permission/admin/manage/modify/service</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>isKDCEnabled</td>
<td>/permission/admin/configure/security,/permission/admin/manage/modify/service</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>listServicePrinciples</td>
<td>/permission/admin/configure/security,/permission/admin/manage/modify/service</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>removeServer</td>
<td>/permission/admin/configure/security,/permission/admin/manage/modify/service</td>
</tr>
<tr class="even">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="odd">
<td><strong>LoggedUserInfoAdmin</strong></td>
<td>getUserInfo</td>
<td>/permission/admin/login</td>
</tr>
<tr class="even">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="odd">
<td><strong>LoggingAdmin</strong></td>
<td>getAllLoggerData</td>
<td>/permission/protected/configure/logging</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getAppenderData</td>
<td>/permission/protected/configure/logging</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getLoggerData</td>
<td>/permission/protected/configure/logging</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getSyslogData</td>
<td>/permission/protected/configure/logging</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getSystemLog</td>
<td>/permission/protected/configure/logging</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>isStratosService</td>
<td>/permission/protected/configure/logging</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>removeSyslogPattern</td>
<td>/permission/protected/configure/logging</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>restoreDefaults</td>
<td>/permission/protected/configure/logging</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>updateAllAppenderData</td>
<td>/permission/protected/configure/logging</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>updateLoggerData</td>
<td>/permission/protected/configure/logging</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>updateSyslogConfig</td>
<td>/permission/protected/configure/logging</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>updateSystemLog</td>
<td>/permission/protected/configure/logging</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="even">
<td><strong>LoginStatisticsAdmin</strong></td>
<td>getLoginAttempts</td>
<td>Not available</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getUserBasedLoginAttempts</td>
<td>Not available</td>
</tr>
<tr class="even">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="odd">
<td><strong>WorkflowAdminService</strong></td>
<td>getWorkflow</td>
<td>/permission/admin/manage/identity/workflow/definition/view</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>listWorkflowEvents</td>
<td>/permission/admin/manage/identity/workflow/association/view</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>listTemplates</td>
<td>/permission/admin/manage/identity/workflow/definition/view</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getTemplate</td>
<td>/permission/admin/manage/identity/workflow/definition/view</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getWorkflowImpl</td>
<td>/permission/admin/manage/identity/workflow/definition/view</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>listWorkflowImpls</td>
<td>/permission/admin/manage/identity/workflow/definition/view</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>addWorkflow</td>
<td>/permission/admin/manage/identity/workflow/definition/create</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>addAssociation</td>
<td>/permission/admin/manage/identity/workflow/association/create</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>changeAssociationState</td>
<td>/permission/admin/manage/identity/workflow/association/update</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>listWorkflows</td>
<td>/permission/admin/manage/identity/workflow/definition/view</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>removeWorkflow</td>
<td>/permission/admin/manage/identity/workflow/definition/delete</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>removeAssociation</td>
<td>/permission/admin/manage/identity/workflow/association/delete</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>listAssociations</td>
<td>/permission/admin/manage/identity/workflow/association/view</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>listAllAssociations</td>
<td>/permission/admin/manage/identity/workflow/association/view</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getEvent</td>
<td>/permission/admin/manage/identity/workflow/association/view</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>getRequestsCreatedByUser</td>
<td>/permission/admin/manage/identity/workflow/monitor/view</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getRequestsInFilter</td>
<td>/permission/admin/manage/identity/workflow/monitor/view</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>deleteWorkflowRequest</td>
<td>/permission/admin/manage/identity/workflow/monitor/delete</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getWorkflowsOfRequest</td>
<td>/permission/admin/manage/identity/workflow/monitor/view</td>
</tr>
<tr class="even">
<td><br />
</td>
<td><br />
</td>
<td><br />
</td>
</tr>
<tr class="odd">
<td><strong>WorkflowImplAdminService</strong></td>
<td>addBPSProfile</td>
<td>/permission/admin/manage/identity/workflow/profile/create</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>listBPSProfiles</td>
<td>/permission/admin/manage/identity/workflow/profile/view</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>getBPSProfile</td>
<td>/permission/admin/manage/identity/workflow/profile/view</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>updateBPSProfile</td>
<td>/permission/admin/manage/identity/workflow/profile/update</td>
</tr>
<tr class="odd">
<td><br />
</td>
<td>removeBPSProfile</td>
<td>/permission/admin/manage/identity/workflow/profile/delete</td>
</tr>
<tr class="even">
<td><br />
</td>
<td>removeBPSPackage</td>
<td>/permission/admin/manage/identity/workflow/profile/delete</td>
</tr>
</tbody>
</table>
