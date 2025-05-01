# Write a Custom Global Scope Validator

WSO2 Identity Server (WSO2 IS) version 5.5.0 and later support configuring scope validators for a service provider. This is a scope validation that can be enforced at the server level. Similar to validators engaged at application level, it has the capability to register multiple validators and execute the chain.

|  | |
| ------ | ------ |
| Usage | A server-level scope validation that has the capability to register multiple validators |
| Interface | `org.wso2.carbon.identity.oauth2.validators.scope.ScopeValidator` |
| Implementation | You can write some classes implementing this interface and register it as a service |

!!! note 
    The following is an optional configuration. If you have some scopes to be allowed without getting validated, this config should be added to the `<IS_HOME>/repository/conf/deployment.toml` file. These scopes will be considered as approved scopes without any validation by the scope validators. 

    ```toml 
    [oauth]
    allowed_scopes = ["scope1", "scope2"]
    ```

---

## Write a custom global scope validator

You can write the custom classes for scope validators by extending the `org.wso2.carbon.identity.oauth2.validators.scope.ScopeValidator` interface.

The following code block is a sample implementation. 

```java
public class CustomScopeValidator implements ScopeValidator {

    /**
     * Validates scopes in the authorization request and manipulate the permitted scopes within the request. Engage
     * it after application-level validators at ResponseTypeHandler level.
     *
     * @param authzReqMessageContext Authorization request.
     * @return True if the user has enough permission to generate tokens or authorization codes with requested
     * scopes or no scopes are requested, otherwise false.
     * @throws IdentityOAuth2Exception Identity Oauth Exception.
     */
    public boolean validateScope(OAuthAuthzReqMessageContext authzReqMessageContext) throws IdentityOAuth2Exception {

        //handle implementation 
        return true;
    }

    /**
     * Validates scopes in the token request and manipulate the permitted scopes within the request. Engage it after
     * application-level validators at GrantHandler level.
     *
     * @param tokenReqMessageContext OAuthTokenReqMessageContext.
     * @return True if the user has enough permission to generate tokens with requested scopes or
     * no scopes are requested, otherwise false.
     * @throws IdentityOAuth2Exception Identity Oauth Exception.
     */
     public boolean validateScope(OAuthTokenReqMessageContext tokenReqMessageContext) throws IdentityOAuth2Exception {

        //handle implementation 
        return true;
     }

    /**
     * Validates the scopes present in the token in the token validation flow.
     * Engage it after application-level validators at TokenValidator level.
     *
     * @param tokenValidationMessageContext OAuth2TokenValidationMessageContext.
     * @return True if scopes present in the tokens are validated successfully, otherwise false.
     * @throws IdentityOAuth2Exception Identity Oauth Exception.
     */
   public boolean validateScope(OAuth2TokenValidationMessageContext tokenValidationMessageContext)
            throws IdentityOAuth2Exception {
       
       //handle implementation
       return true;
   }

    /**
     * Get the friendly name of the implemented scope validator.
     *
     * @return Name of the scope validator.
     */
   public String getName() {
       
       return "CustomGlobalScopeValidator";
   }
}
```

The custom scope validator needs to be registered as an OSGI bundle.

---

## Deploy and configure the custom scope validator

Follow the instructions given below to deploy and enforce the custom global scope validator in WSO2 IS.

1.  Compile the custom global scope validator code and get the resulting .jar file.

2.  Copy the .jar file into the `<IS_HOME>/repository/components/dropins` folder.


## Try out the sample scope validator

1. Build [this](https://github.com/wso2/samples-is/tree/master/scope-validator/sample.scope.validator) sample using maven `mvn clean install`
2. Copy the `sample.scope.validator-1.0.0.jar` binary file from `target` directory into `<IS_HOME>/repository/components/dropins` directory
3. Restart WSO2 IS

This sample application removes the scopes that start with `test` prefix from the authorization request and token request.