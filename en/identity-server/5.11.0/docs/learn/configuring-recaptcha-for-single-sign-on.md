# Configuring reCaptcha for Single Sign On

This topic guides you through configuring reCaptcha for the single sign
on flow. By configuring reCaptcha, you can mitigate or block brute force
attacks.

!!! Info 
    -   For more information on configuring single sign on, see [Configuring
    Single Sign-On](../../learn/configuring-single-sign-on).
    -   For more information on brute force attacks, see [Mitigating Brute
    Force Attacks](../../administer/mitigating-brute-force-attacks).

1.  Set up reCaptcha with the WSO2 Identity Server. For instructions on
    how to do this and more information about reCaptcha, see [Setting Up
    ReCaptcha](../../learn/setting-up-recaptcha).

    !!! tip
    
        To modify the filter mapping for reCaptcha, open the
        `           web.xml          ` file located in the
        `           <IS_HOME>/repository/conf/tomcat/carbon/WEB-INF          `
        directory and find the following filter. You can modify the relevant
        URL patterns if required.
    
        ``` xml
        <filter>
                <filter-name>CaptchaFilter</filter-name>
                <filter-class>org.wso2.carbon.identity.captcha.filter.CaptchaFilter</filter-class>
            </filter>
            <filter-mapping>
                <filter-name>CaptchaFilter</filter-name>
                <url-pattern>/samlsso</url-pattern>
                <url-pattern>/oauth2</url-pattern>
                <url-pattern>/commonauth</url-pattern>
                <dispatcher>FORWARD</dispatcher>
                <dispatcher>REQUEST</dispatcher>
            </filter-mapping>
        ```

2.  Start the WSO2 IS Server and login to the management console.
3.  Click **List** under **Identity Providers** found in the **Main**
    tab.
4.  Click **Resident Identity Provider** and expand the **Login Attempts Security** tab. Then, expand the **reCaptcha for SSO Login** tab.
5.  Select the relevant option according to your requirement:

    - **Always prompt reCaptcha:** 

        Select this option to prompt users for reCaptcha with every SSO login attempt. 

    - **Prompt reCaptcha after max failed attempts:** 
    
        Select this option to prompt reCaptcha only after the number of max failed attempts has been exceeded. 
    
        If this option is selected, enter a value for the **Max failed attempts for reCaptcha** field as well. For example, if you enter 3, reCaptcha will be re-enabled after 3 failed attempts.  
        ![configure-captcha-for-sso](../assets/img/learn/recaptcha-sso.png)
        
        Note the following when selecting this option:
        
        - Account locking must be enabled to enable **Prompt reCaptcha after max failed attempts**.

        - The **Max failed attempts for reCaptcha** value must be lower than the **Maximum failed login attempts** value configured under the **Account Lock** tab.
    
            ![configure-account-locking](../assets/img/tutorials/configure-account-locking.png)
    

6.  You have now successfully configured reCaptcha for the single sign
    on flow. If the number of failed attempts reaches the maximum
    configured value, the following reCaptcha window appears.  

    ![captcha-login-failed](../assets/img/tutorials/captcha-login-failed.png)
