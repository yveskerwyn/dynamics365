# Configure Chat Widget

Make sure you have followed the steps in [Provision Omnichannel for Customer Service](Provision-Omnichannel-for-Customer-Service).

Go to the **Omnichannel Administration** app via [Power Apps Maker Portal](https://make.powerapps.com) or via the [Dynamics 365 Home](https://home.dynamics.com/) - shown hereunder:

> Make sure to select the **Omnichannel Administration** app in the correct environment.

![screenshot](images/omnichannel-admin-select-environment.png)

Verify wether there is a **Live chat workstream** listed in the **Workstreams**:

![screenshot](images/omnichannel-admin-workstreams.png)

![screenshot](images/omnichannel-admin-live-chat-workstream.png)

Go to **Channels** > **Chat**:

![screenshot](images/omnichannel-admin-active-chat-widgets.png)

Click **New** to create a chat widget:

![screenshot](images/omnichannel-admin-new-chat-widget.png)

Specify a name for the widget, e.g. **Customer Portal Chat**, specify **English**  as the language, make sure the work stream is set to the **Live chat workstream**, and hit **Save**:

![screenshot](images/omnichannel-admin-new-chat-widget-save.png)

Copy the **code snippet** code:

![screenshot](images/omnichannel-admin-new-chat-widget-code-snippet.png)

From the **Power Apps Maker Portal** open the **Portal Management** app:

![screenshot](images/omnichannel-maker-portal-apps.png)

![screenshot](images/omnichannel-portal-management.png)

Go to **Content** > **Content Snippets**, and find the **Chat Widget Code**:

![screenshot](images/omnichannel-portal-management-chat-widget-code.png)

Open the **Chat Widget Code**, go to the HTML tab, paste the code snippet from the Chat Widget here, and click **Save**:

![screenshot](images/omnichannel-portal-management-chat-widget-code-save.png)


<script id="Microsoft_Omnichannel_LCWidget" src="https://oc-cdn-public-eur.azureedge.net/livechatwidget/scripts/LiveChatBootstrapper.js" data-app-id="9eb6f398-d0fe-4db0-8f19-df42a72d055c" data-org-id="20ac3d64-eb5e-4871-a345-552c906c8ce9" data-org-url="https://org1a454a99-crm4.omnichannelengagementhub.com"></script>

## Documentation

- [Quickly configure a chat widget](https://docs.microsoft.com/en-us/dynamics365/omnichannel/administrator/configure-live-chat)

## Troubleshooting

- [Clear the server-side cache for a portal](https://docs.microsoft.com/en-us/powerapps/maker/portals/admin/clear-server-side-cache)

  > Create user and assign him to to Administrators role and then login to the portal with following with https://<portal_path>/_services/about:

  ![screenshot](images/omnichannel-troubleshooting-create-user-with-admin-role.png)

- [Chat widget does not load on the portal](https://docs.microsoft.com/en-us/dynamics365/omnichannel/troubleshoot-omnichannel-customer-service#chat-widget-does-not-load-on-the-portal)

  > Make sure a location record exists - which might not be the case as shown hereunder:

  ![screenshot](images/omnichannel-troubleshooting-location-record.png)

  > Add a location record - here seris-demo.powerappsportals.com (**DO NOT INCLUDE HTTTPS**):

  ![screenshot](images/omnichannel-troubleshooting-add-location-record.png)

- [Chat widget icon does not load on the portal](https://docs.microsoft.com/en-us/dynamics365/omnichannel/troubleshoot-omnichannel-customer-service#chat-widget-icon-does-not-load-on-the-portal)

   > Make sure the Logo URL is correct: https://oc-cdn-ocprod.azureedge.net/livechatwidget/images/chat.svg

  ![screenshot](images/omnichannel-troubleshooting-logo-url.png)

- [Chat not getting initiated on starting a new chat from portal](https://docs.microsoft.com/en-us/dynamics365/omnichannel/troubleshoot-omnichannel-customer-service#chat-widget-icon-does-not-load-on-the-portal)

 ## Next

 [Test Omnichannel for Customer Service](Test-Omnichannel.md)