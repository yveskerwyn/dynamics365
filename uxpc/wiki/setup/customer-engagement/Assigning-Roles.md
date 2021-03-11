# Assign Dynamics 365 Roles

[[_TOC_]]

## First add your users to your environment (organization)

> For more details see the documentation: [Create users and assign security roles](https://docs.microsoft.com/en-us/power-platform/admin/create-users-assign-online-security-roles)

Go to the **Power Platform admin center** via https://aka.ms/ppac or http://admin.powerplatform.com/

![image.png](images/assign-roles-ppac-environments.png =700x)

Click **+New** to add a new environment:

![image.png](images/assign-roles-ppac-new-environment.png =700x)

Give your new environment a name, e.g. **CE Trail**, then select **Trial (Subscription-based)** as type, and click **Next**:

![image.png](images/assign-roles-ppac-new-environment-name.png =700x)

Specify a **URL** for your new environment, choose **Yes** for the option to **Enable Dynamics 365 apps**:

![image.png](images/assign-roles-ppac-new-environment-enable-dynamics-365-apps.png =700x)

Under **Automatically deploy these apps** select **All enterprise applications** from the list of available options, and then click **Save**:

![image.png](images/assign-roles-ppac-new-environment-all-enterpise-apps.png =700x)

As result your new environment will get prepared:

![image.png](images/assign-roles-ppac-new-environment-getting-prepared.png =700x)

After a while you can click **Refresh** which will show that your new trial environment got successfully created:

![image.png](images/assign-roles-ppac-new-environment-successfully-created.png =700x)

> Trying to add a database to the default environment and enabling the Dynamics 365 apps is not supported.

> You will get this: 

> ![image.png](images/assign-roles-ppac-adding-database-to-default-environment-not-supported.png =700x)


> Also note that trying to create a new environment of type **Production** will not work

> You will get this:

> ![image.png](images/assign-roles-ppac-created-new-production-environment-not-supported.png =700x)

## Make sure all your users are listed

Click the newly created environment will bring you to following screen:

![image.png](images/assign-roles-ppac-new-environment-details.png =700x)

Click **Settings**:

![image.png](images/assign-roles-ppac-new-environment-settings.png =700x)

Expand the section **Users + permissions** and click **Users**:

![image.png](images/assign-roles-ppac-new-environment-users.png =700x)

Normally all the users that you assigned licenses to will be listed here, you might need to wait a little though and refresh.

In case all users are indeed list you can skip the next section and proceed immediatelly to the steps documented in the section about assigning security roles.

On the other hand, as it typically turns out, one user might be missing; that is you. In that case add yourself following the instructions below.

## Add users

In case no users are listed yet or a user is missing from the list click **+ Add user**:

![image.png](images/assign-roles-ppac-new-environment-add-user.png =700x)

Specify the user you want to add:

![image.png](images/assign-roles-ppac-new-environment-select-user.png =700x)

Click **Add**:

![image.png](images/assign-roles-ppac-new-environment-add-selected-user.png =700x)

Next you are invited to assign a security role:

![image.png](images/assign-roles-ppac-new-environment-new-user-assign-security-role.png =700x)

Click **Go to Dynamics 365** in order to assign security roles to your new user as documented hereunder.

## Assign security role(s)

In order to assign security roles we need to use the legacy **Advanced Settings** pages.

The legacy **Advanced Settings** pages are available via following url, make sure to replace **{your-environment-name}**:

https://{your-environment-name}.crm4.dynamics.com/main.aspx?settingsonly=true

At this point it is possible that the legacy **Advanced Settings** pages are in Dutch:

![image.png](images/assign-roles-advanced-settings-dutch.png =700x)

You will most probably want to change this to English.

In order to change the language click **Settings** (Instellingen) and under **System** (Systeem) click **Administration** (Beheer):

![image.png](images/assign-roles-advanced-settings-dutch-system-administration.png =700x)

Next click on **Languages** (Talen), which will bring up the **Language Settings** (Taalinstellingen) pop-up window:

![image.png](images/assign-roles-advanced-settings-dutch-system-administration-languages.png =700x)

Select **English** (Engels) and then click **Apply** (Toepassen):

![image.png](images/assign-roles-advanced-settings-dutch-system-administration-languages-change-to-english.png =700x)

Confirm the change by clicking **OK** on the next pop-up window:

![image.png](images/assign-roles-advanced-settings-dutch-system-administration-languages-change-to-english-confirm.png =700x)

This will take awhile to complete...

Once completed users can go to their **Personal Settings** and change their language from the **Languages** tab:

![image.png](images/assign-roles-personal-settings-languages.png =700x)

we can now finally assign roles to our users - in English.

In the legacy **Advanced Settings** pages click **Settings** and then under **System** click **Security**:

![image.png](images/assign-roles-advanced-settings-system-security.png =700x)

Next click **Users**:

![image.png](images/assign-roles-advanced-settings-system-security-users.png =700x)

Here select the **Full Access Users** view:

![image.png](images/assign-roles-advanced-settings-system-security-users-full-access-users-view.png =700x)

Select all users and then click **Manage Roles** in the menu:

![image.png](images/assign-roles-advanced-settings-system-security-users-manage-roles.png =700x)

This will bring up the **Manage User Roles** dialog window:

![image.png](images/assign-roles-ppac-new-environment-new-user-manage-user-roles.png =700x)

Choose following roles - other role can be assigned later:

- Customer service app access
- Customer Service Representative
- Customer Voice Add-on
- Dynamics 365 App for Outlook User
- Knowledge Manager
- Marketing Manager
- Marketing Professional
- Omnichannel *** (3x)
- Sales, Enterprise app access

## Access you first Dynamics 365 app through the legacy Dynamics 365 Home page

Go to the legacy https://home.dynamics.com/ and click **Sync**, this will bring up all Dynamics 365 apps you have access to based on the security0 roles assigned to you:

![image.png](images/assign-roles-dynamics-365-home.png =700x)

Scroll down  and pin the **Sales Hub** app:

![image.png](images/assign-roles-dynamics-365-home-pin-sales-hub.png =700x)

Scroll up again and click the **Sales Hub** app that you just pinned:

![image.png](images/assign-roles-dynamics-365-home-select-pinned-sales-hub.png =700x)

## Access you first Dynamics 365 app through the legacy Dynamics 365 Home page

Go to https://portal.office.com, click **All Apps** icon, and then click the **Business Apps** tab:

![image.png](images/assign-roles-business-apps.png =700x)

From there you can click the **Sales Hub** app.

## Assert that users have access to the applications

Have your users browse to the **Dynamics 365 Apps** page with following URL: https://{your-domain}.crm4.dynamics.com/main.aspx?forceUCI=1&pagetype=apps

![dynamics-365-my-apps](images/dynamics-365-my-apps.png =700x)

> Note that **forceUCI=1** forces the use of the **Unified Client Interface**.

From here you can always check the security roles to give access to each of the applications by clicking **MANAGE ROLES** from the menu that appears when clicking the ellipsis:

![dynamics-365-my-apps-manage-roles](images/dynamics-365-my-apps-manage-roles.png =700x)

Here for instance you see all security roles that give access to the **Field Service** app:

![dynamics-365-my-apps-manage-roles-field-service](images/dynamics-365-my-apps-manage-roles-field-service.png =700x)

The **Dynamics 365 Apps** page can also be accessed from any of the Dynamics 365 apps by clicking the gear icon the top right corner, then navigating to **Advanced Settings** and choosing **Apps** from the **Settings** menu:

![dynamics-365-advanced-settings-apps](images/dynamics-365-advanced-settings-apps.png =700x)

![dynamics-365-advanced-settings-apps-published-apps](images/dynamics-365-advanced-settings-apps-published-apps.png =700x)
dynamics-365-advanced-settings-apps-published-apps.png

## Next

Follow the steps documented in [Outlook Integration](Outlook-Integration.md).