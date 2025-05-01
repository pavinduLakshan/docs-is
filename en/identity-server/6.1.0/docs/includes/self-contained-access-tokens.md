### Self-contained access tokens

Optionally, you can configure WSO2 Identity Server to issue [self-contained acccess tokens](../references/concepts/authorization/access-token) for any of the known OAuth 2.0 grant types.

1. Add the following configuration to the `<IS_HOME>/repository/conf/deployment.toml` file.

    ```toml
    [oauth.token_generation]
    access_token_type= "self_contained" 
    ```

2. Restart WSO2 Identity Server.

3. Initiate an access token request to the WSO2 Identity Server, over a known grant type. 

    You will receive a JWT self-contained access token in response to the request. 