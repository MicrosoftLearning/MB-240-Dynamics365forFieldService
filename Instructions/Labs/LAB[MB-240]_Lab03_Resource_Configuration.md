---
lab:
    title: 'Lab 3: Creating resources (20 minutes)'
    module: 'Module 1: Configure Field Service'
---

# Practice Lab 3 - Creating resources
## Scenario
Contoso Coffee uses both internal employees as well as external contractors to perform commercial installation and service existing products. Internal resources are dispatched out of central locations. External resources are dispatched from their location. Ou have been asked to configure Dynamics 365 Field Service to support this. You must add the following:
- Organizational Unit the following locations
    - Bellevue
    - Redmond
    - Tacoma

- Create the following resources:
    -  Internal resources
    - External resources 

## Exercise 1 – Base location

In this exercise you will create the locations where internal resources will start and end their day.  Each organizational unit must have a Latitude and Longitude associated with it to ensure travel times can be calculated accordingly. 

You will need to add the following Organizational Unit locations:
- Bellevue
- Redmond
- Tacoma

### Task 1 - Set Time Zone

1. Click the **Settings** icon in the navigation bar and select **Personalization Settings**.

1. Select your **Time Zone** and click **OK**.

1. Click on **Home** at the top of the left-hand side navigation.

1. In the **Dynamics 365 Field Service app**, click the **Service** area in the bottom-left of the sitemap, and in the **Scheduling** group select **Schedule Board**.

1. Click on the **Scheduler Settings** gear icon on the Schedule Board.

1. Select your **Time Zone**

### Task 2 - Create Organizational Unit

1. In the **Dynamics 365 Field Service app**, click the **Settings** area in the bottom-left of the sitemap, and in the **General** group select **Org Units**.

1. Click **+ New**.

1. Enter **Org Unit** for **Name**.

1. Select the **Scheduling** tab.

1. Enter **47.70939** for Latitude and **-122.31784** for Longitude.

1. Click **Save & Close**

### Task 3 - Create a Warehouse for a Truck

1. In the **Dynamics 365 Field Service app**, click the **Inventory** area in the bottom-left of the sitemap, and in the **Inventory** group select **Warehouses**.

1. Click **+ New**.

1. Enter **Truck** for **Name**.

1. Click **Save & Close**

## Exercise 2 – Configure resources
In this exercise you will define the resources that will perform the onsite work. It is important that any internal resources start and end their day from the Bellevue organizational unit. External contractors will start and end their day from the address associated with their contact record. 

In this exercise, you will be creating:
- An internal resource associated with your user. 
- An external resource associated with a Contact record. 

Both resources will be assigned skills and Characteristics which will be used to identify them as qualified resources when scheduling work orders. 

### Task 1 - Create a Bookable Resource for your user record

1. In the **Dynamics 365 Field Service app**, click the **Resources** area in the bottom-left of the sitemap, and in the **Resource** group select **Resources**.

1. Select the user record you are signed in as ex. **mollyc** or **Molly Clark** for the **User**.

1. Select your Time Zone for **Time Zone**.

1. Select the **Scheduling** tab.

1. Select **Organizational Unit Address** from the **Start Location** drop-down field.

1. Select **Organizational Unit Address** from the **End Location** drop-down field.

1. Select the **Org Unit** organizational unit you created in Exercise 1 for **Organizational Unit**.

1. Select the **Field Service** tab

1. Set the **Hourly Rate** field to **175**.

1. Select the **Truck** you created in Exercise 1 for **Warehouse**.

1. Select **Yes** from the **Time Off Approval Required** drop-down field.

1. Click **Save**.

1. Select the **General** tab

1. If Resource Characteristics are not shown in a sub-grid on the General tab, click **Related** and select **Resource Characteristics**.

1. Click **+ New Bookable Resource Characteristic**.

1. Select the **Building Security** you created in the previous lab for **Characteristic**.

1. Select the **Level 5 Security** you created in the previous lab for **Rating Value**.

1. Click **Save and Close**.

1. Click **+ New Bookable Resource Characteristic**.

1. Select the **CISM** you created in the previous lab for **Characteristic**.

1. Select the **Proficient** you created in the previous lab for **Rating Value**.

1. Click **Save and Close**.

1. Click **+ New Bookable Resource Characteristic**.

1. Select the **CISSP** you created in the previous lab for **Characteristic**.

1. Select the **Expert** you created in the previous lab for **Rating Value**.

1. Click **Save and Close**.

1. Select the **General** tab

1. If **Resource Category Assns** are not shown in a sub-gird on the General tab, click **Related** and select **Resource Category Assns**.

1. Click **+ New Bookable Resource Category Assn**.

1. Select the **Installation Specialist** you created in the previous lab for **Resource Category**.

1. Click **Save & Close**.

1. Click **+ New Bookable Resource Category Assn**.

1. Select the **Security Analyst** you created in the previous lab for **Resource Category**.

1. Click **Save and Close**.

1. Click **Related** and select **Resource Territories** under the **Related-Details** section.

1. Click **+ New Resource Territory**.

1. Select the **North** record you created in the previous lab for **Territory**.

1. Click **Save & Close**.

1. Click the **Work Hours** tab.

1. In the Calendar view, click **+ New** drop-down arrow and select **Working hours**.

1. Select the first of the current month for the date.

1. Select **Every Week** from the **Repeat** drop-down field.

1. Check **Mo** thru **Fr** are checked

1. Uncheck **Su** and **Sa**.

1. Set the Work Hour are set to **9:00 AM** to **5:00 PM**

1. Select your Time Zone.

1. Click **Save**.

1. Click **Save & Close**.

### Task 2 - Create a Working Hours template

1. In the **Dynamics 365 Field Service app**, click the **Resources** area in the bottom-left of the sitemap, and in the **Resource** group select **Work Hours Templates**.

1. Click **+ New**.

1. Enter **Standard hours** for **Name**.

1. Select your user for **Template resource**.

1. Click **Save & Close**.
