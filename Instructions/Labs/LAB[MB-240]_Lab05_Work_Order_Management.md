---
lab:
    title: 'Lab: Work order management'
    module: 'Module 5: Inventory and Work Order Management'
---

Module 5 - Inventory and Work Order Management
=====================
## Practice Lab 5 - Work order management

## Scenario

Worldwide Industries (WWI) provides IT and networking services to their
customers. Their services range from phone system and network installations to
telephoning systems and security system installations. They are going to be
leveraging Dynamics 365 for Field Service for installation and servicing of
these systems for their customers. You are the system implementer that has been
tasked with configuring the application to support the roll-out of the
application. You will be adding and configuring some products that can be
installed and setting up skills and characteristics that will be used as part of
the implementation.

Exercise 1 – Generating Work Orders
===================================

### Task 1 - Create a new work order using and incident type

Lab Setup

1. Go to **Settings** and sekect **Work Order Types** under **Work Orders**.

2. In the name Field enter *Inspection*.

3. Set the Incident Required and Taxable to **No**.

4. Set the Price List to **Default**

4. Click **Save & Close**.

5. Under **Work Orders** go to *Incident Types*.

6. Click **+New**.

7. In the name field type *Install IOT*.

7. Click the **Details** tab and under **Default Work Order Type**, select **Inspection**.

8. Select **Yes** for Copy Incident Items to Agreement.

9. Click **Save & Close**.

10. Under Work Orders, click **Priorities**.

11. Click **+ New**.

12. In the name felid type *Moderate*.

13. Click **Save & Close**.

Out of the box, Dynamics 365 for Field Service has the work order entity enabled
for use with the Resource Scheduling feature. In this task, we will be creating
a new work order that we can schedule using the application.

1.  In **Dynamics 365**, click the arrow next to the **Dynamics 365** text, and
    select **Field Service**.

2.  Click the **Site Map** in the bottom left and select **Service**.  Select **Work Orders** under **Scheduling**

3.  Click the **New** button.

4.  Configure the work order as follows:

    -   **Service Account:** *[your prefix ex. mollyc]+ Account*.  If not found, Click + New Account and enter: [your prefix ex. mollyc]+ Account

    -   **Work Order Type:** *Inspection*

    -   **Taxable:** *No*

    -   **Primary Incident Type:** *Install IOT*

5.  Click the Settings tab, and Configure as follows:

    -   **Priority:** *Moderate* (if necessary, create a new priority with the
        title Moderate and save and close)

    -   **Service Territory:** *[your prefix ex. mollyc]+ North*

    -   **Time from Promised:** *Today \@ 1:00 PM*

    -   **Time to Promised:** *Today \@ 3:00 PM*

6.  **Save and Close** the work order

**Note:** The reason that we selected Install IOT for the incident type is
because incident types are used in Field Service to assist in pre-population
of data when a work order is created. The MRI Inspection incident type was
created previously and has several service tasks, products, services, and
characteristics associated with it.

When a work order is created that uses the Install IOT incident type, this
information is auto populated to the work order. A Dynamics 365 workflow populates this information for us when
the record is saved. It can take several minutes for this to populate.

### Task 2 - Schedule the work order using the schedule board

Field Service provides several items that can be used to assist in scheduling
resources for specific items. The two primary components that are used are the
Schedule Board and the Schedule Assistant. The Schedule Board provides the
ability to manually schedule items, and the assistant offers suggestions on
resources based on factors like location, skills, and availability. In this task
we will examine how you can use the schedule board to schedule items and a high
level.

1.  Select **Schedule Board** under **Scheduling**.

2.  The Schedule Board provides several options that can be used to schedule
    items, such as a filter, and a map view.

3.  Expand the **Booking Requirements** pane at the bottom of the board.

4.  Select **Unscheduled work orders**.

5.  Locate the **work order** for Adventure Works (Sample) that you created in a
    previous task. Drag it to your user's row on the schedule board.

Notice that it the text will appear red until you find a time that falls
within the time window promised.
