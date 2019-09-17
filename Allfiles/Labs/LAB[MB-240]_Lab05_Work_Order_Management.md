Practice Lab 5 - Work Order Management
========================

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

1.  On Virtual machine MIA-BI (unless otherwise specified by your lab hoster),
    sign in as Student with the password Pa55w.rd.

2.  Outside the VM (in the online lab interface), click Files and choose D365
    Credentials. This will allocate a Dynamics 365 tenant for you to use in
    these labs. It will display the admin email and password for your tenant.
    You should copy this information to notepad or similar for your reference.

3.  Navigate in the browser to the Power platform admin portal at
    <https://admin.powerplatform.microsoft.com>. Use the D365 Credentials you
    just acquired in the previous step to login.

4.  Go into the left-hand column and expand Admin Centers and click on Dynamics
    365.

5.  If prompted to select a trial, select the far-right option to install all
    applications.

    1.  **Note:** If you have already selected your trial in a previous lab
        exercise, you will be taken to the D365 Administration Center. If so,
        select the **Open** circled arrow button beside “Contoso Production.”

6.  When viewing tiles of all available applications, click on “Field Service”
    to open your Dynamics 365 instance to the Field Service application. You
    have now entered your Dynamics 365 production environment and are ready to
    explore the Field Service app.


Exercise 2 – Generating Work Orders
===================================

### Task 1 - Create a new work order using and incident type

Out of the box, Dynamics 365 for Field Service has the work order entity enabled
for use with the Resource Scheduling feature. In this task, we will be creating
a new work order that we can schedule using the application.

1.  In **Dynamics 365**, click the arrow next to the **Dynamics 365** text, and
    select **Field Service**.

2.  Click the **Site Map** Icon to expand the **Navigation**. From the menu that
    appears select **work orders**.

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

1.  Click the **Site Map** icon to expand the **Navigation**. From the menu that
    appears select **Schedule Board**.

2.  The Schedule Board provides several options that can be used to schedule
    items, such as a filter, and a map view.

3.  Expand the **Booking Requirements** pane at the bottom of the board.

4.  Select **Unscheduled work orders**.

5.  Locate the **work order** for Adventure Works (Sample) that you created in a
    previous task. Drag it to Allison Dickson’s row on the schedule board.

Notice that it the text will appear red until you find a time that falls
within the time window promised.

1.  Release the mouse button and the item will be placed on the schedule board.

2.  Locate and select the work order for **Fourth Coffee (Sample)** under
    **Unscheduled work orders.** Click **Find Availability**.

3.  Dynamics 365 will analyze the requirements needed for this item and will
    factor in other items such as any skills required, work order & resource
    locations, and resource availability to create a list of suggested resources
    that would be able to work on this item.

4.  As you hover over the available time block for **Van Amundson**, a **Book**
    icon will appear. Click the **Book** icon to schedule Van for this work
    order.

5.  Click the **Exit Search** Icon to return to the Schedule Board.

### Task 3 - Working with the Map View

Another way that items can be scheduled is by using the map view on the Schedule
Board. When you select the map view, resources will be color coded. Any
unscheduled items, will appear on the map with a question mark. You can schedule
these items by dragging them to a specific resource that you want to assign it
to.

As you start assigning items to resources, the item will change to the color of
the resource selected. Additionally, the map will begin to plot a route for the
resource based on the location of the work orders assigned to them.

Additional items like traffic and road maps can be overlaid on the map to assist
in scheduling.

**Notes:** If mapping is not enabled in your tenant, you will receive an error
upon choosing Map View. To enable mapping, click on **Resource Scheduling** in
the left column and select **Administration.** In the Scheduling Settings
section, select **Scheduling Parameters.** Switch the **Connect to Maps** field
to Yes.

1.  On the Schedule Board, click the **Map View**.

2.  To see Traffic, click the **Show Traffic** Icon.

3.  Locate an item on the map that is unscheduled. Drag the item to open time
    slot on Allison Dickson’s schedule right before the work order you scheduled
    for her previously.
