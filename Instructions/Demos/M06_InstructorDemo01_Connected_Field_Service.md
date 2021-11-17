---
lab:
    title: 'Demo: Connected Field Service'
    module: 'Module 6: Customer assets and connected devices'
---

# Demo - Connected Field Service

## Scenario

Worldwide Industries (WWI) provides IT and networking services to their customers. Their services range from phone system and network installations to telephoning systems and security system installations. They are going to be leveraging Dynamics 365 for Field Service for installation and servicing of these systems for their customers. You are the system implementor that has been tasked with configuring the application to support the rollout of the application.

In this Module 6 demo, you deploy Connected Field Service with Azure IoT Hub and then show how devices are connected.

> [!NOTE]
> You require an Azure subscription to perform this demo. If you do not have an Azure subscription a recording of this demo is available to use instead.

## Exercise 1 - Prepare Azure services

In this exercise you will create the Azure services to speed up the deployment of Connected Field Service. You should perform these step these resources prior to the course.

Atr the beginning of the demo to the class show these resources to the class and explain that you have created them to speed up the deployment of connected field service components.

### Task 1 – Create Resource group

1. Access <https://portal.azure.com> and log in with your Azure credentials.

1. Click on **Resource Groups**.

1. Click **+ Create**.

1. Select your Azure subscription.

1. Enter **ConnectedFieldService** for **Resource group**.

1. Select **East US** for **Region**.

1. Click **Review + Create**.

1. Click **Create**.

1. Click on **Home**.

### Task 2 – Azure IoT Hub

1. Click **+ Create a resource**.

1. Enter and then select **IoT Hub** in **Search services and marketplace**.

1. Click **Create**.

1. Select your Azure subscription.

1. Select **ConnectedFieldService** for **Resource group**.

1. Enter **d365cfs** followed by MMDD for the month and year and your initials for **IoT hub name**. The IoT hub name must be unique globally.

1. Select **East US** for **Region**.

1. Select the **Management** tab.

1. Select **S1: Standard tier** for **Pricing and scale tier**

1. Click **Review + Create**.

1. Click **Create**.

1. Click on **Home**.

### Task 3 – Azure storage account

1. Click **+ Create a resource**.

1. Enter and then select **Storage account** in **Search services and marketplace**.

1. Click **Create**.

1. Click **here** for **If you need to create a legacy storage account type**.

1. Select your Azure subscription.

1. Select **ConnectedFieldService** for **Resource group**.

1. Enter **d365cfssa** followed by MMDD for the month and year and your initials for **name**. The storage account name must be unique globally.

1. Select **East US** for **Location**.

1. Select **Standard** for **Performance**.

1. Select **StorageV1 (general purpose v1)** for **Account kind**.

1. Select **Read-access geo-redundant storage (RA-GRS)** for **Redundancy**.

1. Click **Review + Create**.

1. Click **Create**.

1. Click on **Home**.

### Task 4 – Azure Service bus

1. Click **+ Create a resource**.

1. Enter and then select **service bus** in **Search services and marketplace**.

1. Click **Create**.

1. Select your Azure subscription.

1. Select **ConnectedFieldService** for **Resource group**.

1. Enter **d365cfssb** followed by MMDD for the month and year and your initials for **name**. The storage account name must be unique globally.

1. Select **East US** for **Location**.

1. Select **Standard** for **Pricing tier**.

1. Click **Review + Create**.

1. Click **Create**.

1. Click on **Home**.

## Exercise 2 - Configure Connected Field Service

In this exercise you will configure Connected Field Service to use the Azure services you created. You should perform these steps as a demo to the class.

### Task 1 – Start the configuration process for Connected Field Service with Azure IoT Hub deployment

1. Access <https://admin.powerplatform.microsoft.com/environments>.

1. Select the **WWLLABnnn** environment, where nnn is a number. This is the shared Dynamics 365 environment where you will be performing all labs and demos.

1. Click **Open environment**.

1. Click on the name of the app in the top left of the application next to Dynamics 365 and from the list of published apps, select the **Connected Field Service** app.

1. When opening the **Connected Field Service** app, a popup dialog should appear. Select the **left icon** for Azure IoT hub. If the popup dialog does not appear, open a new tab in your browser and navigate to <https://iotdeployment.dynamics.com/>.

1. If a permission requested dialog appears, click **Consent on behalf of your organization** and click **Accept**.

### Task 2 – Select Dynamics 365 environment

1. Check the box for **Terms of Service**.

1. Check the box for  **Microsoft Privacy Statement**.

1. Select the **WWLLABnnn** environment, where nnn is a number.

1. Click **Next**.

### Task 3 – Select Azure subscription

1. Verify that you are signed into the correct Azure account. If not, click **Sign in to a different account**.

1. Select your Azure subscription.

1. Click **Next**.

### Task 4 – Select Azure resource group

1. Enter **cfsresources** for **Resource group name**.

1. Select **East US** for **Resource group location**.

1. Click **Next**.

### Task 5 – Azure resources

1. Check the box for **Use existing Azure resources**.

1. Select the IoT hub you created in Exercise 1 for **IoT Hub**.

1. Select the storage account you created in Exercise 1 for **Storage account**.

1. Select the Service bus you created in Exercise 1 for **Service Bus**.

1. Click **Deploy**.

1. Click **Show details**.

1. Wait for deployment to complete.

### Task 6 – Authorize Azure app connection

1. Click **Authorize Connector in Azure**.

1. In the Azure portal **commondataservice API connection**, select **Edit API connection**.

1. Click **Authorize**.

1. Sign in with your Dynamics 365 tenant credentials.

1. Click **Save**.

### Task 7 – Scale Azure tiers

1. In the IoT Deployment App, click **Open Azure resource group containing all deployed resources**.

1. Select **ServicePlan**.

1. Select **Scale up (App Service plan).

1. Click **Dev/Test**.

1. Select **F1** and click **Apply**.

### Task 8 – Get URL for Simulator

1. In the IoT Deployment App, click **Open device simulator web application**.

1. Verify that Connection Status is **Connected**. If it not connected, click on the Connection tab and enter the name and key of the IoT hub as explained in <https://docs.microsoft.com/dynamics365/field-service/installation-setup-iothub#step-4-set-up-the-simulator-optional>.

1. Save the URL to the simulator.

## Exercise 3 - Configure simulator device

In this exercise you will add an asset and a device to Dynamics Field Service and then register the device in Azure IoT.

### Task 1 – Create a device

1. In the **Connected Field Service** app, click the **Settings** area in the bottom-left of the sitemap, and in the **Settings** group select **Device Categories**.

1. Click **+ New**.

1. Enter **Thermostat Simulator** for **Name**.

1. Click **Save & Close**.

1. In the **Connected Field Service** app, click the **Connected Field Service** area in the bottom-left of the sitemap, and in the **Connected Devices** group select **Devices**.

1. Click **+ New**.

1. Enter **SIM** followed by your initials for **Name**.

1. Select any account.

1. Select the **Thermostat Simulator** device category you created for **Category**.

1. Enter **SIM** followed by your initials for **Device ID**.

1. Click **Save**.

1. In the **Connected Field Service** app, click the **Connected Field Service** area in the bottom-left of the sitemap, and in the **Connected Devices** group select **Customer Assets**.

1. Click **+ New**.

1. Enter **Simulator** for **Name**.

1. Select the **[your prefix] Printer** asset category you created for **Category**.

1. Select the same account used when creating the device.

1. Click **Save**.

### Task 2 – Register the device

1. In the Customer asset record, click **Register Devices** and click **OK**.

1. Once the device has registered, navigate to the Azure portal and view the IoT hub resource.

1. Select **Devices** and verify the device you created in Connected Field Service is listed.

### Task 3 – Configure the Simulator

1. Navigate to the Simulator web application URL.

1. Click **Refresh**.

1. Select the device you created in Connected Field Service. After a short while messages will be sent.

## Exercise 4 - Generate IoT alerts

In this exercise you will use the simulator to generate alerts for Dynamics 365 Field Service and send commands from Connected Field Service to the device.

### Task 1 – Generate an IoT alert

1. Navigate to the Simulator web application URL.

1. Use the mouse to increase the temperature to 100 degrees and humidity to 60 percent.

1. In the **Connected Field Service** app, click the **Connected Field Service** area in the bottom-left of the sitemap, and in the **Connected Devices** group select **Devices**.

1. Open the simulated device. The temperature and humidity should be displayed in the tiles and an IoT alert should have been generated.

1. Select the Alerts tab.

1. Open the IoT Alert and review the data.

1. Return to the device record.

### Task 2 – Send commands to device

1. Click **Send Command**.

1. Enter **{"CommandName":"Reset Thermostat","Parameters":{}}** for **Message** and click **Send Command**.

1. Navigate to the Simulator web application URL.

1. After a short while the simulator will reboot.

1. Use the mouse to increase the temperature to 120 degrees.

1. In the **Connected Field Service** app, another IoT alert should have been generated.

1. Click **Send Command**.

1. Enter **{"CommandName":"Notification","Parameters":{"Message":"Technician has been dispatched"}}** for **Message** and click **Send Command**.

1. Navigate to the Simulator web application URL.

1. After a short while the message will be displayed.
