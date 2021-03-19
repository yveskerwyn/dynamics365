# Outlook Integration

For users to be eligible for the **Microsoft Dynamics 365 App for Outlook** Office add-in they need to:
- Have server-side synchronization set up on the users' mailboxes for incoming emails, appointments, contacts and tasks
- Have the **Dynamics 365 App for Outlook User** security role assigned

## Set up server-side synchronization

Navigate to https://{your-environment-name}.crm4.dynamics.com/main.aspx?settingsonly=true or from your **Dynamics 365 Sales Hub** app click **Advanced Settings**:

![image.png](images/outlook-integration-dynamics-365-sales-hub-advanced-settings.png)

Go to **Settings** | **System** | **Administration**:

![image.png](images/outlook-integration-advanced-settings-administration.png)

Click **System Settings**:

![image.png](images/outlook-integration-advanced-settings-administration-system-settings.png)

First, on the **Email** tab, update default synchronization method for **Appointments, Contacts, and Tasks** to **Server-Side Synchronization**:

![image.png](images/outlook-integration-advanced-settngs-administration-system-settings-update-email-defaults.png)

Make sure (as shown above) that the **Server Profile** is set to **Microsoft Exchange Online**, and then click **OK**.

Next go to **Settings** | **System** | **Email Configuration**:

![image.png](images/outlook-integration-advanced-settngs-system-email-configuration.png)

Here click **Mailboxes**:

![image.png](images/outlook-integration-advanced-settings-email-configuration-mailboxes.png)

You might get the following message, indicating that you have pending email approvals:

![image.png](images/outlook-integration-approve-email-addresses-required-notification.png)

Click **Close** and select the **All Mailboxes** view:

![image.png](images/outlook-integration-advanced-settings-email-configuration-all-mailboxes.png)

> Also see the steps as documented in [https://docs.microsoft.com/en-us/power-platform/admin/connect-exchange-online#configure-mailboxes](https://docs.microsoft.com/en-us/power-platform/admin/connect-exchange-online).

Select the mailboxes of all the users you created, click **Apply Default Email Settings** and then confirm the changes:

![image.png](images/outlook-integration-advanced-settings-email-configuration-apply-defaults.png)

Next, with still all the mailboxes selected, click **Activate**:

![image.png](images/outlook-integration-advanced-settings-email-configuration-activate.png)

Confirm that you want to activate the selected mailboxes:

![image.png](images/outlook-integration-advanced-settings-email-configuration-confirm-activation.png)

Switch back to the **Active Mailboxes** view and see the result:

![image.png](images/outlook-integration-advanced-settings-email-configuration-active-mailboxes.png)

Open the settings for your own mailbox:

![image.png](images/outlook-integration-advanced-settings-email-configuration-mailbox-settings.png)

Notice the warnings in yellow:
- By enabling this command, you consent to share your data with an external system. Data imported from external systems into Microsoft Dynamics 365 are subject to our privacy statement that can be accessed here. Please consult the feature technical documentation for more information.
- Email won't be processed for this mailbox until the email address of the mailbox is approved by an Office 365 Global Administrator or by an Exchange Administrator. For more information, contact your system administrator.
- This mailbox is disabled for incoming email processing. For more information, see the alerts.

Double check that the **synchronization method** for **Incoming Email**, **Outgoing Email** and **Appointments, Contacts, and Tasks** is set to **Server-side synchronization**:

![image.png](images/outlook-integration-advanced-settings-email-configuration-server-side-synchronization.png)

Also make sure the **Server Profile** is set to **Microsoft Exchange Online**.

Click **Save**.

Click **Approve Email**:

![image.png](images/outlook-integration-advanced-settings-email-configuration-approve-email.png)

Confirm that you want to approve the primary email addresses:

![image.png](images/outlook-integration-advanced-settings-email-configuration-confirm-approve-email.png)

Notice that one of the warnings (the second) disappeared:

![image.png](images/outlook-integration-advanced-settings-email-configuration-email-approved.png)

Click **Test & Enable Mailbox**:

![image.png](images/outlook-integration-advanced-settings-email-configuration-test-and-enable-mailbox.png)

Click **OK** in the **Test Email Configuration**  dialog that pops up:

![image.png](images/outlook-integration-advanced-settings-email-configuration-confirm-test-and-enable-mailbox.png)

Click **Save & Close**.

As a result you will receive an e-mail:

![image.png](images/outlook-integration-your-mailbox-is-connected-email.png)

Go back to the **Email Configuration**:

![image.png](images/outlook-integration-advanced-settings-email-configuration-progress.png)

After a while click **Refresh** and assert that the test was successful for your mailbox.

Do the same for all other mailboxes where you wish to enable the add-in.

As a result you get confirmation that the tests ran successfully:

![image.png](images/outlook-integration-advanced-settings-email-configuration-tests-ran-successfully.png)

## Activate the Outlook Add-in

For the next steps you need to have assigned the **Dynamics 365 App for Outlook User** security role to all your users as documented in [Assign Roles](Assigning-Roles).

Go to the **Dynamics 365 App for Outlook** settings:

![image.png](images/outlook-integration-advanced-settings-dynamics-365-app-for-outlook.png)

![image.png](images/outlook-integration-advanced-settings-dynamics-365-app-for-outlook-getting-started.png)

Check the option to **Automatically add Dynamics 365 App for Outlook to all eligible users** and click **Save**:

![image.png](images/outlook-integration-advanced-settings-dynamics-365-app-for-outlook-auto-add-to-all-eligible-users.png)

Select all eligible users and click **Add App for all Eligible Users**:

![image.png](images/outlook-integration-advanced-settings-dynamics-365-app-for-outlook-add-to-all-eligible-users.png)

As a result you'll see this:

![image.png](images/outlook-integration-advanced-settings-dynamics-365-app-for-outlook-adding-to-all-eligible-users.png)

And when finished:

![image.png](images/outlook-integration-advanced-settings-dynamics-365-app-for-outlook-added-to-all-eligible-users.png.png)


## Next

[Teams Integration](Teams-Integration.md)