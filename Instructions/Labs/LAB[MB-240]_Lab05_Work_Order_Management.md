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

This lab will provide you with an actual Dynamics 365 tenant and licenses for
the Power Platform applications you will be using in this course. You will only
be provided with one tenant for the practice labs in this course. The settings
and actions you take within this tenant do not roll-back or reset, whereas the
Windows 10 virtual machine you are provided with will reset each time you close
the lab session. Please keep in mind that Dynamics 365 is evolving all the time.
The instructions in this document may be different from what you experience in
your actual Dynamics 365 tenant.

**Important Note:** If you have already logged into your VM and tenant,
installed your sample data, and enabled Maps recently and are using the same
Dynamics 365 credentials, the virtual machine might pick up where you left off
and you will not need to perform these setup actions. In that case you can skip
ahead to **Exercise 2.**

Exercise 1 - Acquire Tenant Information and Connect
======

## Task 1 – Connect to the Power platform administration portal

1.  Sign into the Virtual Machine using the lab instructions provided by the lab hoster (if using).

2.  Outside the VM in the online lab interface click Files and choose D365
    Credentials. This will allocate a Dynamics 365 365 tenant for you to use in these
    labs.  It will display the user email and password for your tenant. 

3.  Launch Microsoft Edge from the taskbar. 

4.  Navigate in the browser to the Power Platform admin portal at https://admin.Powerplatform.microsoft.com.

5. Sign in using the provided credentials. Record the characters before the "@" symbol in your email address - it should be a first name and a last initial. These characters will become your "alias" throughout the course. Write them down somewhere you'll be able to access throughout the course.

**Important:** Please be aware that this tenant and the Dynamics 365 organization will be shared with the other students in your classroom, like employees would share a tenant when using the Dynamics 365 instance belonging to their organization. Do not use any PII (personally identifiable information) when creating records. It is also good practice to use your username prefix (ex., **mollyc**) in front of all records, data, apps, workflows, etc. you create.

6. Click the button to the left of the **Power Platform admin center** in the top menu to view all available apps. Select **Dynamics 365.**

Select the Field Service app from the list.


Exercise 2 – Generating Work Orders
===================================

### Task 1 - Create a new work order using and incident type

Out of the box, Dynamics 365 for Field Service has the work order entity enabled
for use with the Resource Scheduling feature. In this task, we will be creating
a new work order that we can schedule using the application.

1.  In **Dynamics 365**, click the arrow next to the **Dynamics 365** text, and
    select **Field Service**.

2.  Click the **Site Map** in the bottom left and select **Service**.  Select **Work Orders** under **Scheduling**

3.  Click the **New** button.

4.  Configure the work order as follows:

    -   **Service Account:** *Adventure Works (Sample)*

    -   **Work Order Type:** *Inspection*

    -   **Taxable:** *No*

    -   **Primary Incident Type:** *Install IOT*

5.  Click the Settings tab, and Configure as follows:

    -   **Priority:** *Moderate* (if necessary, create a new priority with the
        title Moderate and save and close)

    -   **Service Territory:** *WA*

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
    previous task. Drag it to Alan Steiner’s row on the schedule board.

Notice that it the text will appear red until you find a time that falls
within the time window promised.
