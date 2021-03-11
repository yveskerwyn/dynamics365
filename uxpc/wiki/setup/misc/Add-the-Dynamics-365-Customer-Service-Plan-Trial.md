# Add the Dynamics 365 Customer Service Plan Trial

[[_TOC_]]

In case you installed a trial of the Dynamics 365 Customer Engagement Plan as documented in [Add the Dynamics 365 Customer Engagement Plan Trial](/setup/Sales/Add-the-Dynamics-365-Customer-Engagement-Plan-Trial) you can skip this step and proceed to [Customer Portal Setup](/setup/Customer-Service/Customer-Portal-Setup).

In case you previously installed a trail of the Sales application as documented in [Setup Dynamics 365 Sales Trial](/setup/Setup-Dynamics-365-Sales-Trial) you will have the Customer Service app installed as part of the Sales app installation.  

**However** that doesn't suffice...

You will need to install a trial of the Customer Service app in a separate environment, since we'll need the **Omnichannel for Customer Service** bits at a later stage of the demo setup, and the only way to get them added to your tenant is by adding trial of the Customer Service app. 

The crucial point in the steps below is to choose for the option to **Create your own trial** instead of the default option to join existing organization (=environment).

By following the steps below you will get a new Customer Service trial in a separate environment. Once installed in a new environment the bits become available to add to your other environments - especially the Omnichannel bits.

Go to https://trials.dynamics.com/Dynamics365/Signup/service:

![image.png](/.attachments/image-40f86840-7e57-4f2d-b4f6-7f7d56b5fe44.png)

Select the option to **Create your own trial**:

![Screenshot 2020-05-07 at 08.07.18.png](/.attachments/Screenshot%202020-05-07%20at%2008.07.18-b052402a-a575-43b8-87e6-945365076b4f.png)

Change the name of the new trial environment that will get created to something meaningful, such as adding a postfix **-customer-service**:

![Screenshot 2020-06-29 at 23.26.57.png](/.attachments/Screenshot%202020-06-29%20at%2023.26.57-2e3553c0-214b-41a1-b98c-5f330082f9a5.png)

![Screenshot 2020-06-29 at 23.31.20.png](/.attachments/Screenshot%202020-06-29%20at%2023.31.20-e1bb372b-0442-41fc-82d5-3ca254aab7df.png)

Click the **Complete Setup** button.

![Screenshot 2020-05-07 at 08.11.10.png](/.attachments/Screenshot%202020-05-07%20at%2008.11.10-7c20d487-6b2e-4ee9-8a59-e9d7bd4a563e.png)

After a while:

![Screenshot 2020-05-07 at 08.14.27.png](/.attachments/Screenshot%202020-05-07%20at%2008.14.27-2c697dd7-af6b-40a7-a9de-28b1d192202a.png)

As a result a new trial environment will been added to your tenant as you can verify in the **Power Apps admin center**: https://admin.powerplatform.microsoft.com/environments

![Screenshot 2020-06-29 at 23.37.08.png](/.attachments/Screenshot%202020-06-29%20at%2023.37.08-78c8be0f-89da-4b85-a73b-73de76554b73.png)

Also when checkin the resources add the tenant level you will see that **Omnichannel for Customer Service** has been added - which we will configure later: https://admin.powerplatform.microsoft.com/resources/applications

![Screenshot 2020-06-29 at 23.39.04.png](/.attachments/Screenshot%202020-06-29%20at%2023.39.04-feaaaff2-412c-4999-9049-75e802b467d0.png)


## Next

Follow the steps documented in [Customer Portal Setup](/setup/customer-service/Customer-Portal-Setup).