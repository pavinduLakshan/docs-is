# Add Passkey login

Based on FIDO concepts, **Passkeys** are a replacement for traditional passwords that allows users to log in to applications without a password using the following methods.
    <ul>
    <li><b>Roaming authenticators</b> - platform-independant FIDO2-supported hardware security keys such as YubiKey.</li>
    <li><b>Platform authenticators</b> - built-in biometrics bound to a single device such as fingerprint scanners or facial recognition features.</li>
    </ul>

Passkeys are phishing resistant and they provide an enhanced user experience as users are not required to manage and remember multiple passwords.

!!! note "What is FIDO2?"
    The FIDO Alliance, whose mission is to reduce the world's reliance on passwords, introduced its latest specifications, collectively called FIDO2. FIDO2 specifications are the World Wide Web Consortium's (W3C) Web Authentication specification (WebAuthn) and FIDO alliance's corresponding Client to Authenticator Protocol (CTAP). Learn more about [FIDO2](https://fidoalliance.org/fido2/){: target="#"}.

There are two types of passkeys based on how they are synchronized.

- **Single-Device Passkeys**

    These passkeys are bound to a single device and are not meant to be shared across multiple devices. Single-device passkeys are useful if you want to reduce the impact of an attack if the credentials are compromised.

- **Multi-Device Passkeys**

    These passkeys enable synchronization across multiple devices allowing users to log into an application from any device, even when their credentials are stored on another.

    Major vendors have already introduced their passkey implementations.

    - Apple users will find their passkeys synced across all devices that are signed into the same Apple ID and iCloud Keychain. Refer to the [Apple documentation](https://developer.apple.com/passkeys/){: target="#"} for more information.

    - Android users will have their passkeys synced across all devices linked to their Google account.  Refer to the [Google documentation](https://developers.google.com/identity/passkeys){: target="#"} for more information.

    If the devices do not sync through the cloud, a user can generate a QR code in the other device and scan it using the device that stores the passkeys to successfully log into the application.

    Refer to the [passkeys documentation](https://passkeys.dev/device-support/){: target="#"} to stay up-to-date with the device support for FIDO2 passkeys.

!!! info
    - {{ product_name }} uses the WebAuthn API to enable FIDO-based authentication for browsers that no longer support the u2f extension.
    - The following browser versions support the WebAuthn API by default:
        - Chrome 67 and above
        - Firefox 60 and above
        - Edge 17723 and above
    - Passkey login with platform authenticators will NOT work on the Firefox browser in macOS Catalina, Big Sur, and Monterey due to browser limitations.
    - Passkey login with roaming authenticators will NOT work on the Firefox browser as the browser doesn't support CTAP2 (Client to Authenticator Protocol 2) with PIN.

The following guide explains how you can enable log in with passkeys in your application.

## Prerequisites

- To get started, you need to [register an application with {{ product_name }}]({{base_path}}/guides/applications/). You can register your own application or use one of the [sample applications]({{base_path}}/get-started/try-samples/) provided.

- You need to have a user account in {{ product_name }}. If you don't already have one, [create a user account]({{base_path}}/guides/users/manage-users/#onboard-a-user) in {{ product_name }}.

## Enable passkey login

{% include "../../../guides/fragments/add-login/passwordless-login/add-passkey-login.md" %}


## Enable passkey progressive enrollment

With passkey progressive enrollment, users can enroll their passkeys on the fly when logging in, offering a blend of convenience and security.

Follow the steps given below to enable passkey progressive enrollment for your application.

1. On the {{ product_name }} Console, go to **Connections**.

2. Select the `Passkey` connection and go to its **Settings** tab.

3. Select the **Allow passkey progressive enrollment** checkbox.

    ![Enable passkey progressive enrollment in {{ product_name }}]({{base_path}}/assets/img/guides/passwordless/passkey/enable-passkey-progressive-enrollment.png){: width="500" style="display: block; margin: 0; border: 0.3px solid lightgrey;"}

4. Click **Update** to save your changes.

5. [Add the passkey progressive enrollment adaptive script]({{base_path}}/guides/authentication/conditional-auth/passkey-progressive-enrollment-based-template) to the login flow of the application.

!!! note
    - If progressive enrollment is disabled, users need to pre-register their passkeys from the MyAccount portal. Learn how to do so in [Register passkeys]({{base_path}}/guides/user-self-service/register-passkey/).

    - Passkey progressive enrollment can only be configured at the organizational level and cannot be modified at the application level.

## Configure passkey usernameless authentication

Usernameless authentication enhances user experience by eliminating the need for users to enter a username during login with passkeys. This is the default behavior in {{product_name}}. Follow the steps given below to configure passkey usernameless authentication for your application.

1. On the {{ product_name }} Console, go to **Connections**.

2. Select the **Passkey** connection.

3. Go to the **Settings** tab of the connection.

4. Select the **Allow passkey usernameless authentication** checkbox to enable usernameless authentication.

    !!! note
        If this option is disabled, users are prompted to enter the username during login with passkeys.

    ![Enable passkey usernameless authentication in {{ product_name }}]({{base_path}}/assets/img/guides/passwordless/passkey/enable-passkey-usernameless-authentication.png){: width="500" style="display: block; margin: 0;border: 0.3px solid lightgrey;"}

5. Click **Update** to save your changes.

!!! note
    Passkey usernameless authentication can only be configured at the organizational level and cannot be modified at the application level.

## Try it out

The following guides let you try out a scenario where, passkey progressive enrollment is **enabled** and passkey usernameless authentication is **disabled**.

### Enroll a passkey

Follow the steps below to enroll a passkey on the fly during login.

1. Access the application URL.

2. Click **Login** to access the {{ product_name }} login page.

3. Select **Sign In With Passkey**.

    ![Sign In with passkey login in {{ product_name }}]({{base_path}}/assets/img/guides/passwordless/passkey/sign-in-with-passkey.png){: width="300" style="display: block; margin: 0; border: 0.3px solid lightgrey;"}

4. To enroll a new passkey, enter your username and select **Create a passkey**.

    ![Create a passkey in {{ product_name }}]({{base_path}}/assets/img/guides/passwordless/passkey/create-passkey.png){: width="300" style="display: block; margin: 0; border: 0.3px solid lightgrey;"}

5. Enter the corresponding password for the user and click **Sign In**.

    ![Basic authenticator in {{ product_name }}]({{base_path}}/assets/img/guides/passwordless/passkey/basic-authenticator.png){: width="300" style="display: block; margin: 0; border: 0.3px solid lightgrey;"}

6. Follow the instructions given by your browser or device to enroll the passkey.

    ![Create a passkey browser prompt in {{ product_name }}]({{base_path}}/assets/img/guides/passwordless/passkey/create-passkey-browser-prompt.png){: width="300" style="display: block; margin: 0; border: 0.3px solid lightgrey;"}

7. Provide a name to uniquely identify your passkey.

    ![Rename passkey in {{ product_name }}]({{base_path}}/assets/img/guides/passwordless/passkey/rename-passkey.png){: width="300" style="display: block; margin: 0; border: 0.3px solid lightgrey;"}

8. Click **Submit** to complete the enrollment. You'll be authenticated in the application.


### Sign in with passkey

Follow the steps below to use an enrolled passkey to sign in to an application.

1. Navigate to the login page of the application.

1. Click  **Login** to access the {{ product_name }} login page.

3. Select **Sign In With Passkey**.

4. Enter your username and select **Continue**.

5. Follow the browser/device instructions to log in with a passkey.

    ![Sign In with passkey browser prompt {{ product_name }}]({{base_path}}/assets/img/guides/passwordless/passkey/sign-in-with-passkey-browser-prompt.png){: width="300" style="display: block; margin: 0; border: 0.3px solid lightgrey;"}

!!! note
    During passkey progressive enrollment, if a user wishes to use a federated authenticator, they should have their external accounts already provisioned within {{product_name}}. If, for example, a user logs in with Google using an account not provisioned in {{product_name}}, passkey enrolment results in an error and the login flow fails.


## Make application a FIDO trusted app

If you wish to integrate passkeys into a mobile application using [app-native authentication]({{base_path}}/guides/authentication/app-native-authentication/), you must validate your application through the validation services provided by the respective platform (iOS or Android). This validation involves associating your application with the identity provider's domain. This association verifies that the authentication requests originate from a legitimate application, protecting against malicious attempts to steal credentials.

{% if product_name == "WSO2 Identity Server" %}

By following this guide, you enable {{product_name}} to host details about your applications in the following endpoints:

- For Android - `{{base_url}}/.well-known/trusted-apps/android`

- For iOS - `{{base_url}}/.well-known/trusted-apps/ios`

The validation services of [iOS](https://developer.apple.com/documentation/xcode/supporting-associated-domains){target="_blank"} and [Android](https://developer.android.com/identity/sign-in/credential-manager#add-support-dal){target="blank"} require application details to be available at the following URLs on your domain,

- For Android - `{your_domain}/.well-known/assetlinks.json`
- For iOS - `{your_domain}/.well-known/apple-app-site-association`

Therefore, make sure these paths of your domain are mapped to the corresponding local endpoints of {{product_name}}.

!!! note

    While not a security concern, it is still important to note that details about your applications are publicly accessible through the endpoints.

    Due to this behavior, you may configure {{product_name}} to display a consent screen for administrators who are attempting to make an application a FIDO trusted app. To do so, add the following configuration to the `deployment.toml` file found in the `<IS_HOME>/repository/conf/` directory.
    
    ```bash
    [application_mgt]
    trusted_app_consent_required=true
    ```
    Once configured, a confirmation popup will appear when enabling the feature and this consent will be recorded and published as an audit log.

To publish app details to the endpoints,

1. On the {{product_name}} Console, go to **Applications** and select your application.

2. In its **Advanced** tab, under **Trusted App Settings**, select **Add as a FIDO trusted app**.

3. Under **Platform Settings**, enter the following platform-specific details.
    
    - For an Android app:

        - Provide the package name of the application which takes the reverse domain format (e.g. com.example.myapp)

        - Provide key hashes, which are SHA256 fingerprints of the app's signing certificate.
    
    - For an iOS app:

        - Provide the app ID of your application which consists of the team ID and the bundle ID separated by a period (.). (e.g. A1B2C3D4E5.com.domainname.applicationname)

4. Click **Update** to save the changes.


{% elif product_name == "Asgardeo" %}
To learn how to implement this, follow the relevant guide based on whether you use Asgardeo domains or custom domains in your organization 

### For Asgardeo domains

It is required by the validation services of [iOS](https://developer.apple.com/documentation/xcode/supporting-associated-domains){target="_blank"} and [Android](https://developer.android.com/identity/sign-in/credential-manager#add-support-dal){target="_blank"} to have details about the application exposed in a public URL. As an Asgardeo domain user, this guide explains how you may publish details about your app to one of the following endpoints of Asgardeo based on the platform.

- For Android - `{{base_url}}/.well-known/assetlinks.json`

- For iOS - `{{base_url}}/.well-known/apple-app-site-association`

!!! warning "Third-party data exposure"
    
    Asgardeo publishes app details to URLs which are common to all organizations. This means your app details will reside together with the app details of other organizations. While this is not a security concern, it is important to note that other organization users may learn details about your applications through these URLs.

    If this is not desirable for your use case, you may use [custom domains]({{base_path}}/guides/branding/configure-custom-domains/) for your organization and publish app details to [custom endpoints](#for-custom-domains).

To publish app details to an Asgardeo endpoint,

1. On the {{product_name}} Console, go to **Applications** and select your application.

2. In its **Advanced** tab, under **Trusted App Settings**, select **Add as a FIDO trusted app**.

3. Under **Platform Settings**, enter the following platform-specific details.
    
    - For an Android app:

        - Provide the package name of the application which takes the reverse domain format (e.g. com.example.myapp)

        - Provide key hashes, which are SHA256 fingerprints of the app's signing certificate.
    
    - For an iOS app:

        - Provide the app ID of your application which consists of the team ID and the bundle ID separated by a period (.). (e.g. A1B2C3D4E5.com.domainname.applicationname)

4. Click **Update** to save the changes.

### For custom domains

It is required by the validation services of [iOS](https://developer.apple.com/documentation/xcode/supporting-associated-domains){target="_blank"} and [Android](https://developer.android.com/identity/sign-in/credential-manager#add-support-dal){target="_blank"} to have details about the application exposed in a public URL. As a custom domain user, you are required to facilitate this by hosting details about your mobile applications in the following endpoints.

- For Android - `{custom_domain}/.well-known/assetlinks.json`

- For iOS - `{custom_domain}/.well-known/apple-app-site-association`

Make sure the data is in the format expected by the validation services of [iOS](https://developer.apple.com/documentation/xcode/supporting-associated-domains){target="_blank"} and [Android](https://developer.android.com/identity/sign-in/credential-manager#add-support-dal){target="_blank"}. 
{% endif %}