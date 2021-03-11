# Customer Portal Setup

[[_TOC_]]

## Create the portal

Go to the **Power Apps Maker Portal**:
http://make.powerapps.com/


Switch to the environment where you set up the Dynamics 365 trials:

![Screenshot 2020-06-26 at 12.10.20.png](images/omnichannel-portal-switch-environment.png =900x)

> It is easy to make a mistake here, e.g. if you created Marketing trial you typically end up with a second environment, make sure not to use that environment

Navigate to the **Create** and scroll down to the **Start from template** section:

![Screenshot 2020-05-06 at 18.40.17.png](images/omnichannel-portal-create-start-from-template.png =900x)

Select the **Customer self-service** template, provided the requested information and **Create**:

![image.png](images/omnichannel-portal-create-customer-self-service-template.png =900x)

![Screenshot 2020-06-26 at 12.16.27.png](images/omnichannel-portal-provisioning-in-progress.png =900x)

Once the portal is ready to use, click **Settings** from the context menu of the portal under **Apps**:

![Screenshot 2020-06-26 at 12.18.27.png](images/omnichannel-portal-settings.png =900x)

This opens open a side pane:

![Screenshot 2020-06-26 at 12.18.42.png](images/omnichannel-portal-settings-side-pane.png =900x)


In this side pane click **Site settings** which will open the **Portal Management** app:

![Screenshot 2020-05-06 at 19.46.06.png](images/omnichannel-portal-management-app.png =900x) 


## Create a portal User

In the **Portal Management** app go to **Contacts**:

![Screenshot 2020-05-06 at 20.12.01.png](images/omnichannel-portal-management-contacts.png =900x)

Click **New**:

In the new contact switch to the **Portal contact** form:

![Screenshot 2020-05-06 at 20.13.02.png](images/omnichannel-portal-managemet-new-contact.png =900x)

Create a new contact Sam De Man with e-mail address sam.deman@outlook.com, and for **Company Name** create a new account record (Aliman):

![Screenshot 2020-05-06 at 20.14.48.png](images/omnichannel-portal-new-contact-details.png =900x)

![Screenshot 2020-05-06 at 20.16.43.png](images/omnichannel-portal-new-contact-quick-create-account.png =900x)

Click **Save** and than click the **Web Authentication** tab:

![Screenshot 2020-05-06 at 20.18.02.png](images/omnichannel-portal-save-new-contact.png =900x)

Enter **sam** as the username for Sam and enable login:

![Screenshot 2020-05-06 at 20.20.08.png](images/omnichannel-portal-new-contact-username.png =900x)

Click **Create Invitation**:

![Screenshot 2020-06-26 at 12.23.35.png](images/omnichannel-portal-new-contact-invitation1.png =900x)

![Screenshot 2020-06-26 at 12.23.35.png](images/omnichannel-portal-new-contact-invitation2.png =900x)

![Screenshot 2020-06-26 at 12.23.35.png](images/omnichannel-portal-new-contact-invitation3.png =900x)

![Screenshot 2020-06-26 at 12.23.35.png](images/omnichannel-portal-new-contact-invitation4.png =900x)

![Screenshot 2020-06-26 at 12.23.35.png](images/omnichannel-portal-new-contact-invitation5.png =900x)

Check the mailbox of Sam Deman:

![Screenshot 2020-06-26 at 12.23.35.png](images/omnichannel-portal-new-contact-invitation6.png =900x)

Click the link will not work, extra configuration is required...

Instead manually set a password...

Next click **Change Password** in the menu and set a password (samLovesD365!!):

![Screenshot 2020-05-06 at 20.27.55.png](images/omnichannel-portal-new-user-change-password.png =900x)

Test the login by visiting the customer portal and clicking Sign-in:

![Screenshot 2020-05-06 at 20.32.26.png](images/omnichannel-portal-new-user-login.png =900x)

This will open the **Profile** page of Sam:

![Screenshot 2020-05-06 at 20.32.26.png](images/omnichannel-portal-nzw-user-profile-page.png =900x)

## Next

[Add a trial of the Dynamics 365 Customer Service Digital Messaging add-on](Add-a-trial-of-the-Dynamics-365-Customer-Service-Digital-Messaging-add%2Don)