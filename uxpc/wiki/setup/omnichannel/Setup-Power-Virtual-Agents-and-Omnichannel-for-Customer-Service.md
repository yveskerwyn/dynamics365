# Setup Power Virtual Agents and Omnichannel for Customer Service

[[_TOC_]]

## Add Power Virtual Agents trial

In the **Microsoft 365 admin center** navigate to **Billing** | **Purchase services** and search for **Power Virtual Agent**:

![screenshot](images/power-virtual-agent.png)

Click the **Power Virtual Agent** tile and then click the **Get free trial** button in the next screen:

![screenshot](images/power-virtual-agent-get-free-trial.png)

Next click the **Try now** button:

![screenshot](images/power-virtual-agent-try-now.png)

And finally click the **Continue** button:

![screenshot](images/power-virtual-agent-continue.png)

As a result you will receive an email:

![screenshot](images/power-virtual-agent-email.png)

## Create bot

Click the **Start your trial >** button in the e-mail you received, this will bring you to the details page of the trial you just added to your tenant:

![screenshot](images/power-virtual-agent-email-start-your-trial.png)

Navigate to http://powerva.microsoft.com/, choose your country/region and click the **Start free trial** button:

![virtual-agent-welcome](images/virtual-agent-welcome.png)

This brings you to the next screen:

![power-virtual-agents](images/power-virtual-agents.png)

Give your first bot a name, e.g. **Demo Bot**, specify **English** as language, and make sure to select your  environment (not the default one) where you setup the Dynamics 365 apps, in our case **Ce Trial - Europe**:

![screenshot](images/power-virtual-agents-new-bot.png)

When you click  **Create**  your bot will be created:

![screenshot](images/power-virtual-agents-new-bot-create.png)

Once created click the **Settings** gear in the top right corner and click the **Transfer to agent** link:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent.png)

Click **Dynamics 365 Omnichannel for Customer Service**:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent-via-omnichannel.png)

Click **Next**:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent-via-omnichannel-next.png)

In the next screen click the **Azure App registration** link:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent-via-omnichannel-azure-app-registration.png)

Click **+ New registration**:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent-via-omnichannel-azure-app-registration-new.png)

Give your app registration a name, e.g. **Demo Bot**, and click **Register**:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent-via-omnichannel-azure-app-registration-register.png)

Copy the **Application (client) ID**:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent-via-omnichannel-azure-app-registration-app-id.png)

Go back to **Power Virtual Agents** tab in your browser, paste the application ID in the **Power Virtual Agents Application ID** field and click **Next**:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent-via-omnichannel-application-id.png)

Click **Next** again:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent-via-omnichannel-next-step.png)

Wait a little:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent-via-omnichannel-wait.png)

Choose your environment, in our case **CE Trial - Europe**, and wait again a little:

![screenshot](images/virtual-agent-choose-environment.png)

When finished close the **Settings** window:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent-close.png)

Navigate to **Topics**:

![screenshot](images/power-virtual-agents-new-bot-topics.png)

![screenshot](images/power-virtual-agents-new-bot-topics2.png)

Click the **Escalate** topic:

![screenshot](images/power-virtual-agents-new-bot-topics-escalate.png)

Click the **Go to authoring canvas** button:

![screenshot](images/power-virtual-agents-new-bot-topics-escalate-authoring-canvas.png)

Delete the **Message** node: 

![screenshot](images/power-virtual-agents-new-bot-topics-escalate-authoring-canvas-delete-node.png)

Add a new **Transfer to agent** node as shown:

![screenshot](images/power-virtual-agents-new-bot-topics-escalate-authoring-canvas-transfer-node.png)

Enter the text the agent should see when the conversation is transferred, e.g. **Escalation from Demo Bot**:

![screenshot](images/power-virtual-agents-new-bot-topics-escalate-authoring-canvas-transfer-node-message.png)

Click **Save**

## Publish the bot

Navigate to **Publish**:

![screenshot](images/power-virtual-agents-new-bot-publish.png)

Click **Publish** and confirm to publish the latest version:

![screenshot](images/power-virtual-agents-new-bot-publish-confirm.png)

## Create an Omnichannel queue for the bot

Navigate to **Apps** in the **Power Apps Maker Portal** and start the **Omnichannel Administration** app from there:

![screenshot](images/omnichannel-admin.png)

First click **Bots** in the **Omnichannel Administration** app and verify that the bot you just created is listed:

![screenshot](images/omnichannel-admin-bots.png)

Navigate to **Queues & Users** | **Queues** and click **New**:

Give the new queue a name, e.g. **Demo Bot queue**, set the **Priority** value to **1** and click **Save**:

![screenshot](images/omnichannel-admin-new-queue.png)

Remove yourself and any other user that might be listed from the **Users (Agents)** list:

![screenshot](images/omnichannel-admin-new-queue-remove-users.png)

Click **Add Existing User**:

![screenshot](images/omnichannel-admin-new-queue-add-existing-user.png)

Add the Demo Bot you created earlier:

![screenshot](images/omnichannel-admin-new-queue-add-existing-user-demo-bot.png)

Click **Save & Close**:

![screenshot](images/omnichannel-admin-new-queue-save-and-close.png)

## Configure the workstream for the chat bot

Navigate to **Work Distribution Management** | **Workstreams** and click **New**:

![screenshot](images/omnichannel-admin-new-workstream.png)

Specify a name for the workstream, e.g. **Demo Bot chat workstream**, from the **Channel** field select the **Live chat** and click **Save**:

![screenshot](images/omnichannel-admin-new-workstream-save.png)

Next we will define a context variable.

Click the **Context Variables** tab and then click **+ New**:

![screenshot](images/omnichannel-admin-workstream-context-variables.png)

Set both the **Display Name** and the **Name** to **va_Scope**, select **Text** as type for this context variable and then click **Save and close**:

![screenshot](images/omnichannel-admin-workstream-context-variable-va_scope.png)

Next based on the value of the context variable **va_Scope** we will route the conversation to the correct queue. We will create two routing roules for this.

The first routing rule is for routing the conversation to the bot, in that case the context variable will not have a value.

Click the **Routing Rules** tab and click **+ Add**:

![screenshot](images/omnichannel-admin-new-workstream-new-routing-rule.png)

Give the new rule a name, e.g. **Demo Bot routing rule**, select the queue you just created and click **Save**:

![screenshot](images/omnichannel-admin-new-workstream-new-routing-rule-save-and-close.png)

Click **+ Condition** and configure the condition as follows and then click **Save & Close**:

![screenshot](images/omnichannel-admin-workstream-routing-rule-for-bot-queue.png)

Now let's create another rule for transferring from the bot to the default (human) queue. In that case the context variable **va_Scope** will have a value (typically "bot").

Click again **+ Add** and give the new rule a name, e.g. **Human routing rule**, and set the queue to the **Default messange queue**:

![screenshot](images/omnichannel-admin-human-rounting-rule.png)

Click **+ Condition** and configure the condition as follows and then click **Save & Close**:

![screenshot](images/omnichannel-admin-workstream-routing-rule-for-human-queue.png)

Again click **Save & Close** to save and close the new workstream.

## Create a new channel for the chat widget

This will be the entry point from the chat widget that will appear on the customer self-service portal.

Navigate to **Channels** | **Chat** and click **+ New**:

![screenshot](images/omnichannel-admin-new-channel.png)

Give chat channel a name, e.g. **Demo Bot chat**, and change the workstream to the work stream you just created:

![screenshot](images/omnichannel-admin-new-channel-name-workstream.png)

Click **Save** and copy the code snippet that was generated for your bot chat widget:

![screenshot](images/omnichannel-admin-new-channel.png)

## Add the chat widget to the customer self-service portal

In the **Power App Maker Portal** navigate to **Apps** and from there start the **Portal Management** app:

![screenshot](images/portal-management.png)

In the **Portal Management** app navigate to **Content** | **Web Templates** and click the **Home** web template: 

![screenshot](images/portal-management-web-templates.png)

Paste the script from the bot chat widget here as shown here and click **Save & Close**:

![screenshot](images/portal-management-web-template-home-paste-script.png)


## Documentation

See:
https://neilparkhurst.com/2020/01/01/omnichannel-for-customer-service-and-power-virtual-agents/

## Next

 [Test Virtual Agent](Test-Virtual-Agent.md)