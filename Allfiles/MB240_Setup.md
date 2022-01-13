# **MB-240 lab setup**

## **Lab Environment**

As this is a shared environment, some tasks that require a tenant Global Administrator or a Service Administrator role will need to be completed by the instructor prior to the course.

## **Bing Maps**

1. Navigate to the Power Platform admin center: <https://admin.powerplatform.microsoft.com/environments>

1. Select the **WWLLABnnn** environment, where nnn is a number. This is the shared Dynamics 365 environment where you will be performing all labs and demos.

1. Click **Settings**.

1. Expand **Product** and select **Features**.

1. Toggle **Bing Maps** to **On**.

1. Click **Save**.

## **Security roles**

1. Navigate to the Power Platform admin center: <https://admin.powerplatform.microsoft.com/environments>

1. Select the **WWLLABnnn** environment, where nnn is a number. This is the shared Dynamics 365 environment where you will be performing all labs and demos.

1. Click **Settings**.

1. Expand **Users + permissions** and select **Security roles**.

1. Select the **Field Service - Administrator** role. There should be 25 users listed. If not click **+ Add people**, search and add the following users.

        Alan Steiner  
        Alicia Thomber  
        Allie Bellew  
        Amy Alberts  
        Anne Weiler  
        Carlos Grilo  
        Christa Geller  
        Dan Jump  
        David So  
        Diane Prescott  
        Eric Gruber  
        Greg Winston  
        Jamie Reding  
        Jeff Hay  
        Julian Isla  
        Karen Berg  
        Kelly Krout  
        Molly Clark  
        Renee Lo  
        Sanjay Shah  
        Spencer Low  
        Sven Mortensen  
        Veronica Quek  
        William Contoso
        System Administrator

1. Select **Security roles**.

1. Select the **Field Service - Resource** role. There should be 25 users listed. If not click **+ Add people**, search and add the same set of users.

## **File attachments**

1. Navigate to the Power Platform admin center: <https://admin.powerplatform.microsoft.com/environments>

1. Select the **WWLLABnnn** environment, where nnn is a number.

1. Click **Settings**.

1. Expand **Email** and select **Email settings**.

1. Enter **131070** for **Maximum file size for attachments**.

1. Click **Save**.

## **Remove sample data**

1. Access <https://admin.powerplatform.microsoft.com/environments>.

1. Select the **WWLLABnnn** environment, where nnn is a number.

1. Click **Open environment**.

1. From the list of available Dynamics 365 apps, select the **Field Service** app.

1. In the **Dynamics 365 Field Service app**, click the **Service** area in the bottom-left of the sitemap, and in the **My Work** group select **Get Started**.

1. Scroll down. If you see **Remove sample data**, click **Remove** and click **Remove sample data**.

1. Wait for the sample data to be removed and the message **Sample data has been removed** to be displayed. Note: This may take some time.

## **Install sample data**

1. Navigate to Field Service Demo Data <https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.48fa2f30-f07d-4474-851d-dda047f15d7b-preview?flightCodes=fsddhide&tab=Overview>

1. Click **Get it now**.

1. Sign in with your Dynamics 365 tenant credentials.

1. Enter your details in the popup dialog, check the box to provide consent and slick **Continue**.

1. Select the **WWLLABnnn** environment, where nnn is a number.

1. Check the boxes to agree to **Legal Terms** and **Privacy Statement**.

1. Click **Install**.

## Enable Bing Maps to use with Resource Scheduling

1. Access <https://admin.powerplatform.microsoft.com/environments>.

1. Select the **WWLLABnnn** environment, where nnn is a number. This is the shared Dynamics 365 environment where you will be performing all labs.

1. Click **Open environment**.

1. From the list of available Dynamics 365 apps, select the **Field Service** app.

1. In the **Dynamics 365 Field Service app**, click the **Resources** area in the bottom-left of the sitemap, and in the **Administration** group select **Scheduling Parameters**.

1. Open the **Resource Scheduling** record.

1. Locate the **Connect to Maps** field. This should be set to **Yes**.

1. If **Connect to Maps** is set to **No**, set it to **Yes** and click **OK** from the popup.

1. Toggle **Enable new Schedule Board** to **On**.

1. Click **Save & Close**.

## Work order settings

1. In the **Dynamics 365 Field Service app**, click the **Settings** area in the bottom-left of the sitemap, and in the **General** group select **Field Service Settings**.

1. If blank, enter **WO** for **Work Order Prefix**.

1. If blank, enter **1000** for **Work Order Starting Number**.

1. Click **Save & Close**.

## Set Time Zone

1. Click the **Settings** icon in the navigation bar od the Field Service app and select **Personalization Settings**.

1. Select your **Time Zone** and click **OK**.

1. Click on **Home** at the top of the left-hand side navigation.

1. In the **Dynamics 365 Field Service app**, click the **Service** area in the bottom-left of the sitemap, and in the **Scheduling** group select **Schedule Board**.

1. Click on the **Scheduler Settings** gear icon on the Schedule Board.

1. Select your **Time Zone**.

1. Set Working time from **06:00 (6:00 AM)** to **20:00 (8:00 PM)**.

1. Click **X** to close **Board view settings**.

## Organizational Unit

1. In the **Dynamics 365 Field Service app**, click the **Settings** area in the bottom-left of the sitemap, and in the **General** group select **Org Units**.

1. Open the **Contoso NA-United States** org unit from the sample data and verify that the **Scheduling** tab contains values for latitude and longitude.

## Configure the instructor resource

1. In the **Dynamics 365 Field Service app**, click the **Resources** area in the bottom-left of the sitemap, and in the **Resource** group select **Resources**.

1. Open the resource for the System Administrator. If there is no resource, click **+ New**, select **User** from the **Resource Type** drop-down field, select the **System Administrator** user, and click **Save**.

1. Select your Time Zone for **Time Zone**.

1. Select the **Scheduling** tab.

1. Select **Organizational Unit Address** from the **Start Location** drop-down field.

1. Select **Organizational Unit Address** from the **End Location** drop-down field.

1. Select the **Contoso NA-United States** organizational unit.

1. Click **Save**.

1. Click **Related** and select **Resource Characteristics**.

1. Click **+ New Bookable Resource Characteristic**.

1. Select the **Smart Brew 300 Master** skill.

1. Click **Save and Close**.

1. Click **Related** and select **Resource Territories**.

1. Click **+ New Resource Territory**.

1. Select the **NA-United States** territory.

1. Click **Save & Close**.

1. Click **Show Work Hours** in the command bar.

1. In the Calendar view, click **+ New** drop-down arrow and select **Working hours**.

1. Select the first of the current month for the date.

1. Select **Every Week** from the **Repeat** drop-down field.

1. Check **Mo** thru **Fr** are checked

1. Uncheck **Su** and **Sa**.

1. Set the Work Hour are set to **9:00 AM** to **6:00 PM**

1. Select your Time Zone.

1. Click **Save**.

1. Click **Save & Close**.

## Create Account

1. In the **Dynamics 365 Field Service app**, click the **Service** area in the bottom-left of the sitemap, and in the **Customers** group select **Accounts**.

1. Click **+ New**.

1. Enter **Litware Coffee** for **Account Name**.

1. Enter **5900 Stewart Ave, Fremont, California 94538, USA** for **Service Address**.

1. Select the **Servicing** tab.

1. Select the **NA-United States** territory for **Service Territory**.

1. Enter **37.51327** for Latitude and **-121.98335** for Longitude.

1. Click **Save & Close**.

## Potential issues

This section describes issues and workarounds.

### BookingStatus entity doesn't contain attribute with Name = msdyn_serviceappointmentstatus

If you see this error when using the Schedule Assistant, you need to install the Service Scheduling solution.

1. Navigate to the Power Platform admin center: <https://admin.powerplatform.microsoft.com>

1. Expand **Resources** and select **Dynamics 365 apps**.

1. Select the ellipses next to **Dynamics 365 Service Scheduling** and select **Install**.

1. Select the **WWLLABnnn** environment, where nnn is a number.

1. Check **I agree to the terms of service** and click **Install**.
