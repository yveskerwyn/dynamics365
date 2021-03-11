# Set Dynamics 365 Customer Engagement Trial

The below documentation is outdated, and is replaced by [Setup Dynamics 365 Customer Engagement Trial](/setup/Setup-Dynamics-365-Customer-Engagement-Trial). 

The below documented steps are best used after having created a Microsoft 365 trial, as documented in [Start with an Office 365 E5 Trial](/setup/Start-with-a-Microsoft-365-E5-Trial).


> However, note that the below steps will fail you, as shown in the very last screenshot here below, so in any case rather go for the option to install trial versions of the engagement apps one by one, starting with the Dynamics 365 Sales app, as documented in [Setup Dynamics 365 Sales Trial](/setup/Setup-Dynamics-365-Sales-Trial).

As a result of following the below steps you **should** (but will not get) a **Dynamics 365 Sales** , **Dynamics 365 Customer Service** and a **Dynamics 365 Field Service** trial all installed in the same environment.

In case you only need a **Dynamics 365 Sales** trial instance you rather  follow the steps as documented in [Setup Dynamics 365 Sales Trial](/setup/Setup-Dynamics-365-Sales-Trial)

Go to Dynamics 365 Trial home page:
https://trials.dynamics.com/

![Screenshot 2020-05-06 at 14.10.47.png](/.attachments/Screenshot%202020-05-06%20at%2014.10.47-0fbb5e4f-84b3-41b2-b838-6fcd104e1e10.png)



> **WARNING** the instructions that follow didn't give the results as expected the last time

> Instead of clicking **Sign up here** here, as documented in what follows, check wether you can add it through the Microft 365 admin center next time, just to see what the best approach is...

**After first having read the above warning**, select **Create your own trial** here:


Scroll down and click the **Sign up here** link:

![Screenshot 2020-05-19 at 11.11.00.png](/.attachments/Screenshot%202020-05-19%20at%2011.11.00-44084f27-3cbd-4561-ac64-9f7b697505e4.png)

This will bring up following dialog:

![Screenshot 2020-05-19 at 11.12.14.png](/.attachments/Screenshot%202020-05-19%20at%2011.12.14-36e3f846-fbf4-45ec-9f67-27412f6f1a05.png)

Click **No, continue signing up**.

In the next screen choose the option **Yes, add it to my account**:

![Screenshot 2020-05-19 at 11.13.35.png](/.attachments/Screenshot%202020-05-19%20at%2011.13.35-984104ac-4d90-4666-a762-b4d1cb438c18.png)]

Click **Try now**:

![Screenshot 2020-05-19 at 11.15.12.png](/.attachments/Screenshot%202020-05-19%20at%2011.15.12-ab995146-12fe-4123-9230-282df4bd7e0c.png)

And then **Continue**:
![Screenshot 2020-05-19 at 11.15.42.png](/.attachments/Screenshot%202020-05-19%20at%2011.15.42-c42d0668-25a5-4172-9e7c-e15d5f633470.png)

As a result you will receive a **Get started with your Dynamics Customer Engagement Plan Trial** mail:

![Screenshot 2020-05-19 at 11.23.49.png](/.attachments/Screenshot%202020-05-19%20at%2011.23.49-92c9d397-d5ff-4076-a945-8058b11a49a7.png)

From this e-mail click the **GET STARTED TODAY** link, which will bring you (you will need to wait 3-5 minutes)  to **Microsoft 365 admin center**:

![Screenshot 2020-05-19 at 11.26.18.png](/.attachments/Screenshot%202020-05-19%20at%2011.26.18-1bc204d1-9e3a-4dd9-ae2e-0c36249b05c3.png)

Here you van follow the steps as documented below, but rather skip immediately to the assign licenses section.

Click the **Go to guided setup** button in the **Finish setting up Dynamics 365 Customer Engagement Plan** tile, which will bring you to the **Microsoft 365 setup wizard**:

![Screenshot 2020-05-19 at 11.28.57.png](/.attachments/Screenshot%202020-05-19%20at%2011.28.57-c0cc0856-a603-49da-8a0e-46cb166d09f8.png)

Clicking the **Advanced setup** link in the upper right corner brings you to following page:

![Screenshot 2020-06-23 at 15.58.09.png](/.attachments/Screenshot%202020-06-23%20at%2015.58.09-e36849dd-cd94-4763-97c5-cb7cb2f921f1.png)
 
Click **Guided setup**.

This basically brings you back to the same page from which you clicked **Advanced setup** - so rather useless:

![Screenshot 2020-05-19 at 11.28.57.png](/.attachments/Screenshot%202020-05-19%20at%2011.28.57-c0cc0856-a603-49da-8a0e-46cb166d09f8.png)

Cliick **Contunue**.

![Screenshot 2020-05-19 at 11.29.34.png](/.attachments/Screenshot%202020-05-19%20at%2011.29.34-d7cc886e-f4b5-4a7d-b853-559b88adfd89.png)

Click **Do this later** - since you already created theses users before. 

![Screenshot 2020-05-19 at 11.30.26.png](/.attachments/Screenshot%202020-05-19%20at%2011.30.26-46b2b331-6ec9-47a7-80d2-893debc4b15d.png)
Click **Go to admin center**.


All the last steps were not really meaningful...

## Assign licenses

Go to **Active Users** and assign the **Dynamics 365 Customer Engagement Plan** license to all the users:

![Screenshot 2020-05-19 at 11.36.38.png](/.attachments/Screenshot%202020-05-19%20at%2011.36.38-599007cb-3115-468c-82a5-644316759505.png)

Click **Dynamics 365 Customer Engagement Plan** and then **Save changes**:

![Screenshot 2020-05-19 at 11.37.44.png](/.attachments/Screenshot%202020-05-19%20at%2011.37.44-96d081f5-3987-41fb-9767-b5e47c406e7c.png)

Also see: [Assigning Licenses](/setup/Assigning-Licenses)

## Add Dynamics 365 Apps

Go to the **Power Platform admin center**:
https://admin.powerplatform.microsoft.com/

Click the default environment:
![Screenshot 2020-05-19 at 11.56.37.png](/.attachments/Screenshot%202020-05-19%20at%2011.56.37-f8892202-0724-4cc9-a4f4-3db5bd32838a.png)

Click **+ Add database**, **Enable Dynamics 365 apps**, and select **Customer Service**, **Field Service** and **Sales Enterprise**, and then click **Add**:

![Screenshot 2020-05-19 at 11.57.36.png](/.attachments/Screenshot%202020-05-19%20at%2011.57.36-d208fb20-6a12-4729-88dc-0e056cbad24e.png)

This will not work for the **default** environment:

![Screenshot 2020-05-19 at 12.01.56.png](/.attachments/Screenshot%202020-05-19%20at%2012.01.56-9f88a4b1-24ce-4da9-8257-cb50713b0afa.png)

So first we need to create a new environment:

![Screenshot 2020-05-19 at 12.03.29.png](/.attachments/Screenshot%202020-05-19%20at%2012.03.29-98f9e79d-02ce-4c08-8bd2-249c551d4ff8.png)

If you choose **trial** you will not be able to enable the Dynamics 365 apps:

![Screenshot 2020-05-19 at 12.06.22.png](/.attachments/Screenshot%202020-05-19%20at%2012.06.22-ec298411-63db-4928-b137-f273d28f4f65.png)

So we need the choose **Production**:

![Screenshot 2020-05-19 at 12.07.12.png](/.attachments/Screenshot%202020-05-19%20at%2012.07.12-ae819d19-5947-4a64-8c1e-9319a55f232f.png)

Change the URL to something you can easily remember, here we have chosen the same name as what we have chosen for the Microsoft 365 trial:

![Screenshot 2020-05-19 at 12.08.04.png](/.attachments/Screenshot%202020-05-19%20at%2012.08.04-bf6fda72-d3ee-4043-a871-997a46f13822.png)

Enable Dynamics 365 apps, select **Customer Service**, **Field Service** and **Sales Enterprise**, and then click **Save**:
![Screenshot 2020-05-19 at 12.10.11.png](/.attachments/Screenshot%202020-05-19%20at%2012.10.11-ae38f0d1-91e2-4af2-80f6-02182b03c314.png)

And this doesn't work:

![Screenshot 2020-06-23 at 16.26.07.png](/.attachments/Screenshot%202020-06-23%20at%2016.26.07-986ec9dd-852e-4e06-834f-d09f6537f1ff.png)

So conclusion: don't use this approach to setup a trial of the customer engagement apps, rather follow the steps as documented in [Setup Dynamics 365 Sales Trial](/setup/Setup-Dynamics-365-Sales-Trial)


## Next
 
Follow the steps documented in [Assigning Roles](/setup/Assigning-Roles).










