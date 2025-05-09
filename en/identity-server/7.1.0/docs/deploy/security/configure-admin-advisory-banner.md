# Admin Advisory Banner Configuration

## Overview
The Admin Advisory Banner feature in {{ product_name }} enhances security by displaying a customizable warning banner during the administrative login process. This ensures that administrators are aware that their session activities are being monitored and logged.

## Configuring the Admin Advisory Banner

Follow the steps below to configure the Admin Advisory Banner:

1. On the {{ product_name }} Console, click the **Root Organization** dropdown at the top and click **Manage Root Organizations**.
2. Click on the gear icon to enter the system settings.
3. Select the **Admin Advisory Banner** tab and turn the **Enabled** toggle on/off to activate/deactivate the advisory banner.
4. Enter the desired warning message in the **Banner content** text box. This message will be displayed on the login page to warn administrators about monitoring policies.
5. Click the **Update** button to save the changes and implement the banner with the specified message.

![Admin Advisory Banner Config]({{base_path}}/assets/img/setup/secure/admin-advisory-banner-config.png){: width="600" style="border: 0.3px solid lightgrey;"}

The advisory banner will appear on the {{ product_name }} Console login page as below, reminding administrators that their credentials are validated through the Identity Server platform and that usage is subject to monitoring.

![Admin Advisory Banner]({{base_path}}/assets/img/setup/secure/admin-advisory-banner.png){: width="300" style="border: 0.3px solid lightgrey;"}
