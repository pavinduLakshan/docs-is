# Exporting WSO2 Identity Server User Information to HubSpot


HubSpot is a customer relationship management solution that brings companies and customers together. 
This topic provides instructions on exporting user data from WSO2 Identity Server (WSO2 IS) to the 
HubSpot platform. 


Let's get started!

!!! tip "Before you begin!"
    Create the `users.csv` file by following the instructions in 
    [Exporting User Data From WSO2 Identity Server](../learn/exporting-user-data-from-wso2-is).
    
## Try it Out

1. Log in into [HubSpot](https://app.hubspot.com/) and access the [contact](https://app.hubspot.com/contacts) section.
2. Click **Import** on the dashboard.
![](../assets/img/tutorials/hubspot-provisioning-user/step-2.png)
3. Select **Start an import**.
![](../assets/img/tutorials/hubspot-provisioning-user/step-3.png)
4. Select **File from computer**. 
![](../assets/img/tutorials/hubspot-provisioning-user/step-4.png)
5. Select **One file**.
![](../assets/img/tutorials/hubspot-provisioning-user/step-5.png)
6. Select **One object**.
![](../assets/img/tutorials/hubspot-provisioning-user/step-6.png)
7. Select **Contacts**.
![](../assets/img/tutorials/hubspot-provisioning-user/step-7.png)
8. Upload the `users.csv` file.
![](../assets/img/tutorials/hubspot-provisioning-user/step-8.png)
9. Map the file columns to contact properties. You can skip columns that do not match.
![](../assets/img/tutorials/hubspot-provisioning-user/step-9.png)
10. Finish the import.
![](../assets/img/tutorials/hubspot-provisioning-user/step-10.png)
11. Once the import is complete, you can check the contacts dashboard to see the imported users.
![](../assets/img/tutorials/hubspot-provisioning-user/step-11.png)
