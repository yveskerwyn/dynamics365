# AI Builder Demo

## Getting started

Make sure you have to demo files copied into your tenant, as documented in [AI Builder Demo Setup](/setup/aibuilder/AI-Builder-Demo-Setup).

Also see, discovered after having created this wiki page: [Object Detection Application with AI Builder and Power Apps](https://radacad.com/object-detector-app-with-ai-builder-and-power-apps)

Start by showing the Excel file in your OneDrive:

![Screenshot 2020-04-08 at 16.59.38.png](images/Screenshot%202020-04-08%20at%2016.59.38-8ca20df0-031a-4866-bd96-c0861d98ddf7.png)

![Screenshot 2020-04-08 at 17.00.35.png](images/Screenshot%202020-04-08%20at%2017.00.35-ea8c61a9-8ae2-4d26-bdfd-b33cf1c3e42d.png)

## Create entity

Go to your [Power Apps Maker Portal](https://make.powerapps.com) and select an environment:

![Screenshot 2020-04-08 at 17.10.07.png](images/Screenshot%202020-04-08%20at%2017.10.07-27351d58-664a-47eb-8963-1e01901b49b9.png)

Under **Data** click **Entities**:

![Screenshot 2020-04-08 at 17.11.42.png](images/Screenshot%202020-04-08%20at%2017.11.42-cd7aea49-0c1a-4c60-8680-7605b611f0be.png)

Create a new entity **mytea**:

![Screenshot 2020-04-08 at 18.15.22.png](images/Screenshot%202020-04-08%20at%2018.15.22-5a801698-f3a4-4502-9618-ddf10674299c.png)

Click the **Keys** tab:

![Screenshot 2020-04-08 at 18.18.29.png](images/Screenshot%202020-04-08%20at%2018.18.29-580e4ee2-4d68-48fb-80d0-4a0558e35424.png)

Create a key, select the existing **Name** field and set the display name to **Name**:

![Screenshot 2020-04-08 at 18.20.33.png](images/Screenshot%202020-04-08%20at%2018.20.33-60e71e59-02cf-4fd4-ae08-a59440b0bf33.png):

Click **Save Entity** at the bottom left of the screen:

![Screenshot 2020-04-08 at 18.23.10.png](images/Screenshot%202020-04-08%20at%2018.23.10-e63273c5-ad18-4cea-8580-a9109bd6fb43.png)

## Get data

Go to the **Data** tab:

![Screenshot 2020-04-08 at 18.22.41.png](images/Screenshot%202020-04-08%20at%2018.22.41-a9cda37b-84bf-4d56-94e0-95f9fb4e9ac0.png)

Click **Get Data**:

![Screenshot 2020-04-08 at 18.24.20.png](images/Screenshot%202020-04-08%20at%2018.24.20-50b9ca44-1acf-462f-adcc-35e54187679a.png)

Select **Excel** from the Power Query data sources:

![Screenshot 2020-04-08 at 18.25.11.png](images/Screenshot%202020-04-08%20at%2018.25.11-7888cd8d-a4f6-4cc8-9ac8-a82d9b397e07.png)

Select the **ProductsAI.xlsx** Excel from your OneDrive, and if required click the blocked pop-up:

![Screenshot 2020-04-08 at 18.27.42.png](images/Screenshot%202020-04-08%20at%2018.27.42-e078c3a7-a39e-40f4-8304-008c7bc3e911.png)

Open the Excel file:

![Screenshot 2020-04-08 at 18.29.00.png](images/Screenshot%202020-04-08%20at%2018.29.00-b49d50d2-fdfc-4830-a5f8-cd3b4313c8be.png)

One the next screen make sure you have valid credentials, of kind **Organizational** and click **Next**:

![Screenshot 2020-04-08 at 18.31.38.png](images/Screenshot%202020-04-08%20at%2018.31.38-732cd79e-e594-4829-b4f7-b65e5302d035.png)

Select **Table1** and click **Transform data**:

![Screenshot 2020-04-08 at 18.32.32.png](images/Screenshot%202020-04-08%20at%2018.32.32-ae3d14f4-37ab-4f4f-ad08-acc8eeca3a33.png)

Keep the query as is in the **Power Query** screen and click **Next**:

![Screenshot 2020-04-08 at 18.34.46.png](images/Screenshot%202020-04-08%20at%2018.34.46-d1fc0ad7-6551-4125-a486-f289b2e0d0b4.png)

In the next step under **Load settings** choose **Load to existing entity** and select the entity you just created as the destination entity, here **cr055_mytea**:

![Screenshot 2020-04-08 at 18.40.39.png](images/Screenshot%202020-04-08%20at%2018.40.39-6e496c9c-1a50-41af-8229-27e3db0d6c56.png)

Still on the same screen under **Field mapping** select **Product** as the source column and click **Next**:

![Screenshot 2020-04-08 at 18.42.26.png](images/Screenshot%202020-04-08%20at%2018.42.26-0a312002-803e-44c0-bca9-d636fcbd3010.png)

In the last step choose **Refresh manually** and click **Create**:

![Screenshot 2020-04-08 at 18.44.15.png](images/Screenshot%202020-04-08%20at%2018.44.15-87b5e5f3-676e-4a7b-88e7-b01de5f1e4dd.png)

Wait and after a little while you can click **Done**.

Click **Refresh data** to have the data from your Excel file loaded:

![Screenshot 2020-04-08 at 18.47.35.png](images/Screenshot%202020-04-08%20at%2018.47.35-132ab6c3-6681-4e99-a2f8-e6e46f3592e9.png)

## Train the AI model

Under **AI Builder** click **Models**:

![Screenshot 2020-04-08 at 18.48.55.png](images/Screenshot%202020-04-08%20at%2018.48.55-3f47e980-c636-43e9-bfa9-18f70ad6ed64.png)

Click **Build an AI model** to create an AI model:

![Screenshot 2020-04-08 at 18.50.35.png](images/Screenshot%202020-04-08%20at%2018.50.35-10fe2107-4401-42d4-b44b-de7ab66afcf7.png)

Optionally, you can click **Start free trial**, but that will happen automatically later.

![Screenshot 2020-04-08 at 18.54.44.png](images/Screenshot%202020-04-08%20at%2018.54.44-3e3f2871-f171-4814-8b94-75c43dc05981.png)

Choose **Object Detection**, and give your model a name, here **myteamodel**:

![Screenshot 2020-04-08 at 18.56.21.png](images/Screenshot%202020-04-08%20at%2018.56.21-bbc456db-ee8f-46f6-8b92-f568af3404b9.png)

Next, in the **Select domain** step choose **Objects on retail shelves** and click **Next**:

![Screenshot 2020-04-08 at 20.18.32.png](images/Screenshot%202020-04-08%20at%2020.18.32-bcfabe2c-4c36-4ec7-a57a-4fff1bd1597b.png)

In the **Choose objects** step, click **Switch to database** in the **Select from database instead** tile under the **Quick tips**:

![Screenshot 2020-04-08 at 20.24.25.png](images/Screenshot%202020-04-08%20at%2020.24.25-20f19007-00d7-4e06-afe1-9c9efc71d73e.png)

Then click **Switch**:

![Screenshot 2020-04-08 at 20.24.53.png](images/Screenshot%202020-04-08%20at%2020.24.53-3b72a70b-8c64-4cc6-96d7-dd32e6e65656.png)

Then click **Select from database**, find and select your enity, here **mytea**:

![Screenshot 2020-04-08 at 20.26.55.png](images/Screenshot%202020-04-08%20at%2020.26.55-72e89fa5-ef6f-414c-99f8-1af48ba686d3.png)

After having selected your entity, select the **Name** field and click **Select Field**:

![Screenshot 2020-04-08 at 20.29.11.png](images/Screenshot%202020-04-08%20at%2020.29.11-28638290-3f44-442b-a42d-35d9e63748ea.png)

**Select all** three product names and click **Next**:

![Screenshot 2020-04-08 at 20.30.22.png](images/Screenshot%202020-04-08%20at%2020.30.22-b2d4cf26-59f0-4630-8275-1fffcd6d0c9a.png)

In the **Add images** step add the demo pictures, by clicking the **Add images** button:

![Screenshot 2020-04-08 at 20.32.00.png](images/Screenshot%202020-04-08%20at%2020.32.00-3acff28a-d63a-4924-8286-12307b2759b2.png)

Choose to get **Add images** from **SharePoint**:

![Screenshot 2020-04-08 at 20.33.49.png](images/Screenshot%202020-04-08%20at%2020.33.49-79ef772a-da46-4df1-8403-a351318f01fa.png)

Click the **View or create connections** button:

![Screenshot 2020-04-08 at 20.34.54.png](images/Screenshot%202020-04-08%20at%2020.34.54-83476361-bb93-4341-bc4e-5f05b1097fdf.png)

Click **+New connection** button :

![Screenshot 2020-04-08 at 20.36.56.png](images/Screenshot%202020-04-08%20at%2020.36.56-10a014e8-cbbb-4b5c-b7f0-f3aebf4df0da.png)

Select **SharePoint**:

![Screenshot 2020-04-08 at 20.37.24.png](images/Screenshot%202020-04-08%20at%2020.37.24-88f7d149-334d-471b-a4ca-5e43e2ee5bba.png)

Choose for the option to **Connect directly (cloud-services)** and click **Create**:

![Screenshot 2020-04-08 at 20.39.19.png](images/Screenshot%202020-04-08%20at%2020.39.19-24c79ab8-6843-4b25-b944-aa92f150c012.png)

Sign in with your account:

![Screenshot 2020-04-08 at 20.40.25.png](images/Screenshot%202020-04-08%20at%2020.40.25-8792c342-7e3d-472c-8297-b34bb8e2cde2.png)

Select the SharePoint connection you just added:

![Screenshot 2020-04-08 at 20.41.27.png](images/Screenshot%202020-04-08%20at%2020.41.27-d0976d96-6d37-42ed-8a6c-2148c71a0f67.png)

Go back to the browser tab or window where you were invited to select a SharePoint connection and click **Refresh** as a result the newly created connection will appear, select it:

![Screenshot 2020-04-08 at 20.44.08.png](images/Screenshot%202020-04-08%20at%2020.44.08-975fbcc1-f0d1-4fb9-a8ee-2544837a84ef.png)

Select the SharePoint site where you saved the demo images:

![Screenshot 2020-04-08 at 20.54.19.png](images/Screenshot%202020-04-08%20at%2020.54.19-60e8de53-c138-4403-8486-9838a38adc47.png)

Find the folder where you uploaded the pictures:

![Screenshot 2020-04-08 at 20.55.46.png](images/Screenshot%202020-04-08%20at%2020.55.46-d111111d-8a8f-42b0-aec3-17b5a136b230.png)

Select all pictures and click **Add**:

![Screenshot 2020-04-08 at 20.56.30.png](images/Screenshot%202020-04-08%20at%2020.56.30-803710db-337f-4b3b-8e71-6b1cf196ba89.png)

Then click **Upload 30 images**:

![Screenshot 2020-04-08 at 20.56.41.png](images/Screenshot%202020-04-08%20at%2020.56.41-97ea58df-2611-4234-be66-f220cc08ec2a.png)
 
Wait until all pictures are uploaded:

![Screenshot 2020-04-08 at 20.57.48.png](images/Screenshot%202020-04-08%20at%2020.57.48-9385c5eb-7fa6-45e0-b15b-c551b2340110.png)

Once done click **Close**:

![Screenshot 2020-04-08 at 20.58.45.png](images/Screenshot%202020-04-08%20at%2020.58.45-23674659-de73-4a82-8e37-03134c8bdac4.png)

Click **Next**:

![Screenshot 2020-04-08 at 20.59.31.png](images/Screenshot%202020-04-08%20at%2020.59.31-ca40efaa-5293-4c9a-9d13-ee19c30b7c68.png)

In the **Tag images** step you will need to tag every image:

![Screenshot 2020-04-08 at 21.00.44.png](images/Screenshot%202020-04-08%20at%2021.00.44-aae79575-b36b-48b7-9da8-860cd7457e7f.png)

Tagging is done by selecting the item and choosing the correct product name:

![Screenshot 2020-04-08 at 21.02.18.png](images/Screenshot%202020-04-08%20at%2021.02.18-a8ed60e6-633c-4509-af99-ce92dc137192.png)

![Screenshot 2020-04-08 at 21.06.16.png](images/Screenshot%202020-04-08%20at%2021.06.16-8cdd0d9e-8c2b-4563-b240-fa49a988f8ff.png)

Once done click **Done tagging**:

![Screenshot 2020-04-08 at 21.07.51.png](images/Screenshot%202020-04-08%20at%2021.07.51-f57e4460-494d-48c3-b4f6-3955d79265bb.png) 

Then click **Next**:

![Screenshot 2020-04-08 at 21.08.51.png](images/Screenshot%202020-04-08%20at%2021.08.51-de411289-70cc-46cd-be54-99f41a0967ff.png)

In the **Model summary** step click **Train**:

![Screenshot 2020-04-08 at 21.10.28.png](images/Screenshot%202020-04-08%20at%2021.10.28-5b49ee4d-a057-436f-b99e-49e18cf46551.png)

Once done, click **Go to models**:

![Screenshot 2020-04-08 at 21.10.57.png](images/Screenshot%202020-04-08%20at%2021.10.57-9df34431-fc25-4fa8-8108-c4652caacf48.png)

It can take a little while before the model is fully trained:

![Screenshot 2020-04-08 at 22.31.52.png](images/Screenshot%202020-04-08%20at%2022.31.52-e598d7eb-9dcb-46b1-a514-c31b3657aef8.png)

Once trained you need to **publish** the model:

![Screenshot 2020-04-08 at 22.33.29.png](images/Screenshot%202020-04-08%20at%2022.33.29-a8fc5c49-98eb-47e7-8d6a-bb07df4bca76.png)

Once published you can use the model:

![Screenshot 2020-04-08 at 22.34.39.png](images/Screenshot%202020-04-08%20at%2022.34.39-4efbdc3a-fdca-442c-ad46-f7d99f7bc015.png)

![Screenshot 2020-04-08 at 22.35.09.png](images/Screenshot%202020-04-08%20at%2022.35.09-1880402f-bc94-406b-bc72-4130217f6b94.png)


## Create a App

Click **+Create** and select **Canvas aap from blank**:

![Screenshot 2020-04-08 at 21.13.46.png](images/Screenshot%202020-04-08%20at%2021.13.46-533b7072-0514-42d8-a799-c670e5e3174e.png)

Give you app a name, choose the **Phone** format and click **Create**:

![Screenshot 2020-04-08 at 21.14.26.png](images/Screenshot%202020-04-08%20at%2021.14.26-6e5e4ca7-3314-4c4b-ba8b-0a562043752c.png)

Skip the **Welcome to Power Apps Studio** screen:

![Screenshot 2020-04-08 at 21.16.36.png](images/Screenshot%202020-04-08%20at%2021.16.36-bc8a2317-4063-4ad1-832c-3a3f127c950a.png)

Choose your region and click **Get started**:

![Screenshot 2020-04-08 at 21.17.38.png](images/Screenshot%202020-04-08%20at%2021.17.38-ee70d0a9-83e8-4476-92be-80245410bda4.png)

**Insert** an **AI Builder** **Object detector**:

![Screenshot 2020-04-08 at 21.21.34.png](images/Screenshot%202020-04-08%20at%2021.21.34-eef599f4-9914-4ab4-9e9e-ea114eac3f87.png)

Acknowledge the message about the premium component:

![Screenshot 2020-04-08 at 21.22.44.png](images/Screenshot%202020-04-08%20at%2021.22.44-15289a64-7c25-441f-8571-0d5d2234122f.png)

Next you will need to select your model:

![Screenshot 2020-04-08 at 21.25.36.png](images/Screenshot%202020-04-08%20at%2021.25.36-c5528f10-03f0-454a-9b78-027a9471e972.png)

At this point your model made not show up because it is still training and/or not published yet...

Once published the model will show up you click **Refresh**:

![Screenshot 2020-04-08 at 22.36.41.png](images/Screenshot%202020-04-08%20at%2022.36.41-84949dd3-72cc-4fed-861c-8a68cb783229.png)

You can test the object detector by **Alt + Clicking** on the detector on the word **Detect** and then select one of the pictures:

![Screenshot 2020-04-08 at 22.40.39.png](images/Screenshot%202020-04-08%20at%2022.40.39-ef482bb4-8d2e-4129-ad2e-3020f9056033.png)

Next **Insert** a vertical gallery:

![Screenshot 2020-04-08 at 21.18.45.png](images/Screenshot%202020-04-08%20at%2021.18.45-2548693b-4477-4337-ade0-0e6b2e8bee9a.png)

Move the vertical gallery below the object detector, and then set its data source to **ObjectDetector1.VisionObjects:

![Screenshot 2020-04-08 at 22.45.41.png](images/Screenshot%202020-04-08%20at%2022.45.41-5593b8ca-8a99-4de7-96ed-71bf1a9fed08.png)

![Screenshot 2020-04-08 at 22.45.53.png](images/Screenshot%202020-04-08%20at%2022.45.53-95ace537-a758-4b71-af9b-f10c23130eca.png)

Change the **Subtitle** Text value to **ThisItem.count**:

![Screenshot 2020-04-08 at 23.04.55.png](images/Screenshot%202020-04-08%20at%2023.04.55-7487a3f8-297a-43c3-9a7b-eb154e2e0714.png)

As a result it will show the number of detected objects:

![Screenshot 2020-04-08 at 23.07.51.png](images/Screenshot%202020-04-08%20at%2023.07.51-51a35251-6e2e-4e05-8f8d-bff3f9ede1e7.png)