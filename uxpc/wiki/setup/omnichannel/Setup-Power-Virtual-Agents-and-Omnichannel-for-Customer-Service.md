# Setup Power Virtual Agents and Omnichannel for Customer Service

[[_TOC_]]

## Add Power Virtual Agents trial

In the **Microsoft 365 admin center** navigate to **Billing** | **Purchase services** and search for **Power Virtual Agent**:

![screenshot](images/power-virtual-agent.png =900x)

Click the **Power Virtual Agent** tile and then click the **Get free trial** button in the next screen:

![screenshot](images/power-virtual-agent-get-free-trial.png =900x)

Next click the **Try now** button:

![screenshot](images/power-virtual-agent-try-now.png)

And finally click the **Continue** button:

![screenshot](images/power-virtual-agent-continue.png)

As a result you will receive an email:

![screenshot](images/power-virtual-agent-email.png =900x)

## Create bot

Click the **Start your trial >** button in the e-mail you received, this will bring you to the details page of the trial you just added to your tenant:

![screenshot](images/power-virtual-agent-email-start-your-trial.png =900x)

Navigate to http://powerva.microsoft.com/:

![screenshot](images/power-virtual-agents.png =900x)

Give your first bot a name, e.g. **Demo Bot**, specify **English** as language, and make sure to select your  environment (not the default one) where you setup the Dynamics 365 apps, in our case **Ce Trial - Europe**:

![screenshot](images/power-virtual-agents-new-bot.png =900x)

When you click  **Create**  your bot will be created:

![screenshot](images/power-virtual-agents-new-bot-create.png =900x)

Once created click the **Settings** gear in the top right corner and click the **Transfer to agent** link:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent.png =900x)

Click **Dynamics 365 Omnichannel for Customer Service**:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent-via-omnichannel.png =900x)

Click **Next**:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent-via-omnichannel-next.png =900x)

In the next screen click the **Azure App registration** link:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent-via-omnichannel-azure-app-registration.png =900x)

Click **+ New registration**:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent-via-omnichannel-azure-app-registration-new.png =900x)

Give your app registration a name, e.g. **Demo Bot**, and click **Register**:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent-via-omnichannel-azure-app-registration-register.png =900x)

Copy the **Application (client) ID**:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent-via-omnichannel-azure-app-registration-app-id.png =900x)

Go back to **Power Virtual Agents** tab in your browser, paste the application ID in the **Power Virtual Agents Application ID** field and click **Next**:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent-via-omnichannel-application-id.png =900x)

Click **Next** again:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent-via-omnichannel-next-step.png =900x)

Wait a little:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent-via-omnichannel-wait.png =900x)

Choose your environment, in our case **CE Trial - Europe**, and wait again a little:

![screenshot](images/virtual-agent-choose-environment.png =900x)

When finished close the **Settings** window:

![screenshot](images/power-virtual-agents-new-bot-transfer-to-agent-close.png =900x)

Navigate to **Topics**:

![screenshot](images/power-virtual-agents-new-bot-topics.png =900x)

![screenshot](images/power-virtual-agents-new-bot-topics2.png =900x)

Click the **Escalate** topic:

![screenshot](images/power-virtual-agents-new-bot-topics-escalate.png =900x)

Click the **Go to authoring canvas** button:

![screenshot](images/power-virtual-agents-new-bot-topics-escalate-authoring-canvas.png =900x)

Delete the **Message** node: 

![screenshot](images/power-virtual-agents-new-bot-topics-escalate-authoring-canvas-delete-node.png =900x)

Add a new **Transfer to agent** node as shown:

![screenshot](images/power-virtual-agents-new-bot-topics-escalate-authoring-canvas-transfer-node.png =900x)

Enter the text the agent should see when the conversation is transferred, e.g. **Escalation from Demo Bot**:

![screenshot](images/power-virtual-agents-new-bot-topics-escalate-authoring-canvas-transfer-node-message.png =900x)

Click **Save**

## Publish the bot

Navigate to **Publish**:

![screenshot](images/power-virtual-agents-new-bot-publish.png =900x)

Click **Publish** and confirm to publish the latest version:

![screenshot](images/power-virtual-agents-new-bot-publish-confirm.png =900x)

## Create an Omnichannel queue for the bot

Navigate to **Apps** in the **Power Apps Maker Portal** and start the **Omnichannel Administration** app from there:

![screenshot](images/omnichannel-admin.png =900x)

First click **Bots** in the **Omnichannel Administration** app and verify that the bot you just created is listed:

![screenshot](images/omnichannel-admin-bots.png =900x)

Navigate to **Queues & Users** | **Queues** and click **New**:

Give the new queue a name, e.g. **Demo Bot queue**, set the **Priority** value to **1** and click **Save**:

![screenshot](images/omnichannel-admin-new-queue.png =900x)

Remove yourself and any other user that might be listed from the **Users (Agents)** list:

![screenshot](images/omnichannel-admin-new-queue-remove-users.png =900x)

Click **Add Existing User**:

![screenshot](images/omnichannel-admin-new-queue-add-existing-user.png =900x)

Add the Demo Bot you created earlier:

![screenshot](images/omnichannel-admin-new-queue-add-existing-user-demo-bot.png =900x)

Click **Save & Close**:

![screenshot](images/omnichannel-admin-new-queue-save-and-close.png =900x)

## Configure the workstream for the chat bot

Navigate to **Work Distribution Management** | **Workstreams** and click **New**:

![screenshot](images/omnichannel-admin-new-workstream.png =900x)

Specify a name for the workstream, e.g. **Demo Bot chat workstream**, from the **Channel** field select the **Live chat** and click **Save**:

![screenshot](images/omnichannel-admin-new-workstream-save.png =900x)

Next we will define a context variable.

Click the **Context Variables** tab and then click **+ New**:

![screenshot](images/omnichannel-admin-workstream-context-variables.png =900x)

Set both the **Display Name** and the **Name** to **va_Scope**, select **Text** as type for this context variable and then click **Save and close**:

![screenshot](images/omnichannel-admin-workstream-context-variable-va_scope.png =900x)

Next based on the value of the context variable **va_Scope** we will route the conversation to the correct queue. We will create two routing roules for this.

The first routing rule is for routing the conversation to the bot, in that case the context variable will not have a value.

Click the **Routing Rules** tab and click **+ Add**:

![screenshot](images/omnichannel-admin-new-workstream-new-routing-rule.png =900x)

Give the new rule a name, e.g. **Demo Bot routing rule**, select the queue you just created and click **Save & Close**:

![screenshot](images/omnichannel-admin-new-workstream-new-routing-rule-save-and-close.png =900x)

Click **+ Condition** and configure the condition as follows and then click **Save & Close**:

![screenshot](images/omnichannel-admin-workstream-routing-rule-for-bot-queue.png =900x)

Now let's create another rule for transferring from the bot to the default (human) queue. In that case the context variable **va_Scope** will have a value (typically "bot").

Click again **+ Add** and give the new rule a name, e.g. **Human routing rule**, and set the queue to the **Default messange queue**:

![screenshot](images/omnichannel-admin-human-rounting-rule.png =900x)

Click **+ Condition** and configure the condition as follows and then click **Save & Close**:

![screenshot](images/omnichannel-admin-workstream-routing-rule-for-human-queue.png =900x)

Again click **Save & Close** to save and close the new workstream.

## Create a new channel for the chat widget

This will be the entry point from the chat widget that will apper on the customer self-service portal.

Navigate to **Channels** | **Chat** and click **+ New**:

![screenshot](images/omnichannel-admin-new-channel.png =900x)

Give chat channel a name, e.g. **Demo Bot chat**, and change the workstream to the work stream you just created:

![screenshot](images/omnichannel-admin-new-channel-name-workstream.png =900x)

Click **Save** and copy the code snippet that was generated for your bot chat widget:

![screenshot](images/omnichannel-admin-new-channel.png =900x)

## Add the chat widget to the customer self-service portal

In the **Power App Maker Portal** navigate to **Apps** and from there start the **Portal Management** app:

![screenshot](images/portal-management.png =900x)

In the **Portal Management** app navigate to **Content** | **Web Templates** and click the **Home** web template: 

![screenshot](images/portal-management-web-templates.png =900x)

Paste the script from the bot chat widget here as shown here and click **Save & Close**:

![screenshot](images/portal-management-web-template-home-paste-script.png =900x)


## Documentation

See:
https://neilparkhurst.com/2020/01/01/omnichannel-for-customer-service-and-power-virtual-agents/

## Next

 [Test Virtual Agent](Test-Virtual-Agent)