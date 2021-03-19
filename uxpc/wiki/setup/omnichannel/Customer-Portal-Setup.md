# Customer Portal Setup

## Create the portal

Go to the **Power Apps Maker Portal**:
http://make.powerapps.com/


Switch to the environment where you set up the Dynamics 365 trials:

![omnichannel-portal-switch-environment](images/omnichannel-portal-switch-environment.png)

> It is easy to make a mistake here, e.g. if you created Marketing trial you typically end up with a second environment, make sure not to use that environment

Click **+ Create** in the left navigation pane and scroll down to the **Start from template** section:

![omnichannel-portal-create-start-from-template](images/omnichannel-portal-create-start-from-template.png)

Select the **Customer self-service** template, provide the requested information and **Create**:

![omnichannel-portal-create-customer-self-service-template](images/omnichannel-portal-create-customer-self-service-template.png)

Wait while your portal gets provisioned:

![omnichannel-portal-provisioning-in-progress](images/omnichannel-portal-provisioning-in-progress.png)

Once the portal is ready to use, click **Settings** from the context menu of the portal under **Apps**:

![omnichannel-portal-settings](images/omnichannel-portal-settings.png)

This opens open a side pane:

![omnichannel-portal-settings-side-pane](images/omnichannel-portal-settings-side-pane.png)


In this side pane click **Site settings** which will open the **Portal Management** app:

![omnichannel-portal-management-app](images/omnichannel-portal-management-app.png) 


## Create a portal User

In the **Portal Management** app go to **Contacts**:

![omnichannel-portal-management-app](images/omnichannel-portal-management-app.png)

Click **New**:

In the new contact switch to the **Portal contact** form:

![omnichannel-portal-managemet-new-contact](images/omnichannel-portal-managemet-new-contact.png)

Create a new contact Sam De Man with e-mail address sam.deman@outlook.com, and for **Company Name** create a new account record (Aliman):

![omnichannel-portal-new-contact-details](images/omnichannel-portal-new-contact-details.png)

![omnichannel-portal-new-contact-quick-create-account](images/omnichannel-portal-new-contact-quick-create-account.png)

Click **Save** and than click the **Web Authentication** tab:

![omnichannel-portal-save-new-contact](images/omnichannel-portal-save-new-contact.png)

Enter **sam** as the username for Sam and enable login:

![omnichannel-portal-new-contact-usernam](images/omnichannel-portal-new-contact-username.png)

Click **Create Invitation**:

![omnichannel-portal-new-contact-invitation1](images/omnichannel-portal-new-contact-invitation1.png)

![omnichannel-portal-new-contact-invitation2](images/omnichannel-portal-new-contact-invitation2.png)

![omnichannel-portal-new-contact-invitation3](images/omnichannel-portal-new-contact-invitation3.png)

![omnichannel-portal-new-contact-invitation4](images/omnichannel-portal-new-contact-invitation4.png)

![omnichannel-portal-new-contact-invitation5](images/omnichannel-portal-new-contact-invitation5.png)

Check the mailbox of Sam Deman:

![omnichannel-portal-new-contact-invitation6](images/omnichannel-portal-new-contact-invitation6.png)

Click the link will not work, extra configuration is required...

Instead manually set a password...

Next click **Change Password** in the menu and set a password (samLovesD365!!):

![omnichannel-portal-new-user-change-password](images/omnichannel-portal-new-user-change-password.png)

Test the login by visiting the customer portal and clicking Sign-in:

![omnichannel-portal-new-user-login](images/omnichannel-portal-new-user-login.png)

This will open the **Profile** page of Sam:

![omnichannel-portal-nzw-user-profile-page](images/omnichannel-portal-nzw-user-profile-page.png)

## Next

[Add a trial of the Dynamics 365 Customer Service Digital Messaging add-on](Add-a-trial-of-the-Dynamics-365-Customer-Service-Digital-Messaging-add%2Don.md)