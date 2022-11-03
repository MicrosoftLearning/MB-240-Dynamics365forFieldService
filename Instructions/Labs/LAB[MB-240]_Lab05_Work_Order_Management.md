---
lab:
    title: 'Lab 5: Work order management  (50 minutes)'
    module: 'Module 2: Manage Work Orders'
---

# Practice Lab 5 - Work order management

## Exercise 1 – Settings for work orders

In this exercise you will configure settings for work orders including priorities and resolutions.

### Task 1 - Priorities

1. In the **Dynamics 365 Field Service app**, click the **Settings** area in the bottom-left of the sitemap, and in the **Work Orders** group select **Priorities**.

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **Low** for **Name**.

1. Select **1** from the **Level of Importance** drop-down field.

1. Enter **6CC6CC** for **Priority Color**.

1. Click **Save & Close**.

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **Normal** for **Name**.

1. Select **4** from the **Level of Importance** drop-down field.

1. Enter **FFA8FC** for **Priority Color**.

1. Click **Save & Close**.

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **High** for **Name**.

1. Select **8** from the **Level of Importance** drop-down field.

1. Enter **FF8E42** for **Priority Color**.

1. Click **Save & Close**

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **Urgent** for **Name**.

1. Select **10** from the **Level of Importance** drop-down field.

1. Enter **FF1C33** for **Priority Color**.

1. Click **Save & Close**.

### Task 2 - Resolutions

1. In the **Dynamics 365 Field Service app**, click the **Settings** area in the bottom-left of the sitemap, and in the **Work Orders** group select **Resolutions**.

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **Replaced Toner** for **Name**.

1. Click **Save & Close**

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **Replaced Printer Drum** for **Name**.

1. Click **Save & Close**

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **Inspection complete no issues** for **Name**.

1. Click **Save & Close**

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **Inspection complete with issues** for **Name**.

1. Click **Save & Close**

## Exercise 2 – Create and process work orders

In this exercise you will create work orders, schedule the work orders, and complete the work orders.

### Task 1 - Create a new work order using an incident type

1. In the **Dynamics 365 Field Service app**, click the **Service** area in the bottom-left of the sitemap, and in the **Scheduling** group select **Work Orders**.

1. Click **+ New**.

1. Select the **[your prefix] Relecloud** account you created in a previous lab  for **Service Account**.

1. Select the **[your prefix] Service Printer** incident type you created in a previous lab for **Primary Incident Type**.

1. Select the **Settings** tab.

1. Select the **[your prefix] Normal** priority you created in Exercise 1 for **Priority**.

1. Select the **[your prefix] North** territory you created in a previous lab **Service Territory**.

1. Select the **[your prefix] Jane Doe** contact you created in a previous lab  for **Reported By Contact**.

1. Enter **Today \@ 1:00 PM** for **Time from Promised**.

1. Enter **Tomorrow \@ 6:00 PM** for **Time to Promised**.

1. Click **Save**.

### Task 2 - Schedule the work order using the schedule assistant

Field Service provides several items that can be used to assist in scheduling resources for specific items. The two primary components that are used are the Schedule Board and the Schedule Assistant. The Schedule Board provides the ability to manually schedule items, and the assistant offers suggestions on resources based on factors like location, skills, and availability. In this task we will examine how you can use the Book button from within the work order.

1. In the work order you created in Task 1, click on the **Book** button in the command bar.

1. Select a time slot and click **Book & Exit**.

### Task 3 - Create and process a work order without using an incident type

1. In the **Dynamics 365 Field Service app**, click the **Service** area in the bottom-left of the sitemap, and in the **Scheduling** group select **Work Orders**.

1. Click **+ New**.

1. Select the **[your prefix] Relecloud** account you created in a previous lab  for **Service Account**.

1. Select the **[your prefix] Inspection** work order type you created in a previous lab for **Work Order Type**.

1. Select the **Settings** tab.

1. Select the **[your prefix] Low** priority you created in Exercise 1 for **Priority**.

1. Select the **[your prefix] North** territory you created in a previous lab **Service Territory**.

1. Select the **[your prefix] Jane Doe** contact you created in a previous lab  for **Reported By Contact**.

1. Enter **10:00 AM** for **Time Window Start**.

1. Enter **2:00 PM** for **Time Window Wnd**.

1. Click **Save**.

1. Select the **Service Tasks** tab.

1. Click **+ New Work Order Service Task**.

1. Select the **[your prefix] Inspection** service task type you created in Task 2 for **Task Type**.

1. Click **Save and Close**.

1. Click **Related** and select **Characteristics**.

1. Click **+ New Requirement Characteristic**.

1. Select the **[your prefix] Building Security** characteristic you created in a previous lab for **Characteristic**.

1. Select the Resource Requirement for the work order. This will have the same number as the Work Order for **Resource Requirement**.

1. Click **Save and Close**.

1. Click **Related** and select **Requirement**.

1. Edit the Resource Requirement record and examine its contents. It should contain the same information on the work order.

1. Navigate back to the work order.

1. In the business process flow, click **Next Stage**. Verify that System Status is **Unscheduled** and Substatus is blank.

1. Click **Book**.

1. Select a time slot and click **Book & Exit**.

1. Click **Refresh** in the command bar. Verify that System Status is **Scheduled**.

1. Click **Related** and select **Requirements**.

1. Edit the Resource Requirement record and examine its contents. Select the **Scheduling** tab. The **Remaining Duration** should be **0 minutes**.

1. Navigate back to the work order.

1. In the Summary tab, edit the booking in the Bookings section and examine its contents.

1. In the Bookable Resource Booking form, select the **General** tab.

1. Set the **Actual Arrival Time** to the **Estimated Arrival Time**.

1. Select the **General** tab and change the **Booking Status** to **In Progress**.

1. Click **Save & Close**.

1. Click **Refresh** in the command bar. Verify that System Status is **In Progress**.

1. In the Summary tab, edit the booking in the Bookings section.

1. In the Booking Record Booking form, change the **Booking Status** to **Completed** and **Save & Close**.

1. Select the **Service Tasks** tab.

1. Edit the service task and set **% Complete** to **100**, **Actual Duration** to **30 minutes** and click **Save & Close**.

1. In the business process flow, click **Next Stage**. Verify that System Status is **Completed**.

1. Select the **Summary** tab.

1. Select the **[your prefix] Inspection complete no issues** resolution you created in Exercise 1 for **Primary Resolution**.

1. Click **Save**.

### Task 4 - Create an incident type from a work order

1. Edit the work order you completed in the previous task.

1. Click **Create Incident Type** in the command bar.

1. Enter **[your prefix ex. mollyc]** + **Quick Inspection** for **Name**.

1. Click **Create Incident Type**.

1. Click **Yes** to the prompt, and inspect the new incident type.
