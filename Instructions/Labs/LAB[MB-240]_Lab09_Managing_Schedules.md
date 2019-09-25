---
lab:
    title: 'Lab: Managing schedules'
    module: 'Module 10: Managing Scheduling Options'
---

Module 10 - Managing Scheduling Options
=====================
## Practice Lab 9 - Managing schedules

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
========================

### Task 1 – Connect to the Power platform administration portal

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

    - **Note:** If you have already selected your trial in a previous lab
        exercise, you will be taken to the D365 Administration Center. If so,
        select the **Open** circled arrow button beside “Contoso Production.”

6.  When viewing tiles of all available applications, click on “Field Service”
    to open your Dynamics 365 instance to the Field Service application. You
    have now entered your Dynamics 365 production environment and are ready to
    explore the Field Service app.

Exercise 2 – Configure supporting resources, roles, and skills
===========================

### Task 1 – Create three resource categories

Before we start making the resource facilities, pools, and requirement groups
that will be used to support the scheduling scenario, we what to ensure that we
have the necessary supporting components defined that will be used to schedule.

To make it as easy as possible we are going to add three resource categories
that can be easily used to identify consultation rooms, patient consultants, and
Doctors.

1.  With the **Field Service** application open, click the Site Map in the
    bottom left corner and select **Resources.**

2.  Open **Categories** in the left menu.

3.  Click the **New** button to create a new Resource Category.

4.  Enter **Consultation Room** into the Name field and select **Save and
    Close.**

5.  Click the **New** button to create another new Resource Category.

6.  Enter **Patient Consultant** into the name field and select **Save and
    Close.**

7.  Click the **New** button to create the last new Resource Category.

8.  Enter **Doctor** into the name field and select **Save and Close**.

### Task 2 – Create a Consultation Characteristic

Some doctors may be able to do consultations, and some may not. To ensure that
we can identify the doctors that are able to perform consultations, we are going
to add a new resource characteristic called Consultation. This characteristic
will be added to any resource that could be used in a consultation.

1.  While you are in **Resources** section, click **Characteristics** in the
    left menu.

2.  Click the **New** button to define a **Characteristic**.

3.  Enter **Consultation** into the Name field. (If prompted to create a new
    Characteristic, press new and create the Characteristic before assigning it
    as a Bookable Resource Characteristic.)

4.  Enter your user record as the Resource.

5.  **Save and close.**

### Task 3 – Configure Resource Working Hours

One factor that goes a long way in ensuring that all resources that will be
working together on projects or as part of a pool have the same working hours.
Work hours can be defined for up to 25 resources at one time by creating a work
hours template. A work hours template must be based on another resource’s
working hours.

We will start by defining the working hours for a single resource. We will use
that resource to create the Work Hours Template, and finally we are going to
apply the template to all our resources.

1.  While you are in **Resources**, click **Resources** in the left menu.

2.  Locate and select the resource record for **Bob Kozak**.

3.  On the **command bar** at the top, click the **Show Work Hours** button.
    *(Note: you may need to allow pop-up windows if you are running a popup
    blocker.)*

4.  Select the **Set-Up** button.

5.  From the menu that appears, select the **New Weekly Work Schedule** option.

6.  When the weekly schedule is displayed, click the **Set Work Hours**
    hyperlink to edit the working hours.

7.  Verify the Work Hours are set to **8:00 AM** to **5:00 PM** and click
    **OK.**

8.  Uncheck the **Saturday** and **Sunday** boxes.

9.  Click **Save and Close** to apply the new work schedule.

10. Verify that the new schedule is being applied moving forward and **Close**
    the **Work Hours window.**

11. In the left menu, click on **Workhour Templates.**

12. Click the **New** button to define a new template.

13. Define the template as follows:

    - **Name:** *Standard Hours*

    - **Template Resource:** *Bob Kozak*

14. Click **Save and Close.**

15. In the left menu, select **Resources.**

16. Highlight the first 25 resources listed in **Active Bookable Resources**
    *(Important: Make sure that Bob Kozak is not one of the resources
    selected)*. Click the **Set Calendar** button.

17. In the **Work template** screen, select the **Standard Hours** template that
    you just created and click **apply**.

18. With those 25 resources still selected, click the **Edit** button. In the
    Time Zone Field, set to the time zone you want to use. Click **Change.**

### Task 4 – Create Facility Resources for Screen Rooms

Now that we have configured the supporting option, we can now configure our
resources to support the functionality we need. We will begin by defining the
consultation rooms that may be used as facility resources.

1.  Using the **SiteMap**, navigate to **Resources**. Click **Resources** in the
    left menu.

2.  Click the **New** button to create a new resource.

3.  Configure the resource as follows:

    -   **Resource Type:** *Facility*

    -   **Facility:** Click Create New. Create a Facility with the following
        characteristics:

        1.  **Name:** *Hospital ABCD*

        2.  **Organizational Unit:** *Seattle*

        3.  **Time Zone:** The time zone you have been using.

        4.  **Save and Close** to return to the Bookable Resource screen and
            continue creating your resource.

    -   **Name:** *Screening Room A*

4.  Select the Scheduling tab, and configure the scheduling settings as follows:

    -   **Organizational Unit:** *Seattle*

    -   **Start Location:** *Organizational Unit Address*

    -   **Start Location:** *Organization Unit Address*

5.  Click the **Save** button to save the new resource and leave it open.

6.  Open the Project Service tab. In the **Resource Skills** sub-grid, select
    the ellipses, and choose **Add Bookable Resource Characteristic.**

7.  Configure the Bookable Resource Characteristic as follows:

    -   **Characteristic:** *Consultation*

    -   **Rating Value:** *Proficient*

8.  Click **Save.**

9.  In the **Resource Roles** sub-grid, select the ellipses and choose **Add
    Bookable Resource Category**.

10. Select Consultation room for the **Resource Category.**

11. Click **Save and Close**.

12. Repeat steps 2 – 12 to define the following resources:

    1.  Screening Room B

    2.  Screening Room C

    3.  Screening Room D

### Task 5 - Create a Facility Resource Pool

There are times when a scheduler just wants to note that a screening room is
needed until they can define the specific room they want to use as more details
about the consultation is captured. The easiest way to accomplish this, is by
using the Resource Pool. We will create a resource pool that will contain all
the facility resource that we just created.

1.  If necessary, navigate to Resources and click the New button to create a new
    Bookable resource.

2.  Define the new Resource as follows:

    -   **Resource Type:** *Pool*

    -   **Pool Type:** *Facility*

    -   **Name:** *Consultation Rooms*

    -   **Time Zone:** *Set to the same as other resources*

3.  Select the Scheduling tab, and configure the Scheduling Options as noted
    below:

    -   **Organizational Unit:** *Seattle*

    -   **Start Location:** *Organizational Unit Address*

    -   **End Location:** *Organizational Unit Address*

4.  Click the **Save** button to save the record and Leave it open.

5.  Locate and select the **Related** tab. From the menu that appears select
    **Resource’s Children**.

6.  Select the **Add New Bookable Resource Group**, and configure as follows:

    -   **Name:** *Screening Room A*

    -   **Parent Resource:** *Consultation Rooms*

    -   **Child Resource:** *Screening Room A*

    -   **From Date:** *Beginning of current Month*

    -   **To Date:** *End of Current month*

7.  Click **Save and Close**

8.  Repeat steps 6 & 7 to add the following items:

    -   Screening Room B

    -   Screening Room C

    -   Screening Room D

### Task 6 - Add Characteristic sand Resource Roles to Resources

Next, we want to ensure that when we search for resources that are qualified to
participate in consultations that we will get some results. To accomplish this,
we are going to define some characteristics, and roles for resources. Each
resource will be assigned the consultation characteristic. We will also edit
each resource to ensure that they are associated with the Seattle Organizational
Unit.

**Doctors:**

-   Abraham McCormick

-   Allison Dickson

-   Ashley Chinn

-   Bernadette Foley

**Patient Consultants:**

-   Cheri Castaneda

-   Christal Robles

-   Christie Dawson

-   Clarence Desimone

1.  If necessary, navigate to **Resources** and open the **Abraham McCormick**
    resource.

2.  In the Project Service tab, locate the **Resource Skills** sub-grid. Select
    the ellipses button and choose **Add Bookable Resource Characteristic.**

3.  Configure the Bookable Resource Characteristic as follows:

    -   **Characteristic:** *Consultation*

    -   **Rating Value:** *Proficient*

4.  Click **Save.**

5.  Locate the **Resource Role** sub-grid, select the more commands button, can
    choose **Add Bookable Resource Category**.

6.  Select **Doctor** for the **Resource Category.**

7.  Click **Save.**

8.  Select the Scheduling tab, and configure the scheduling as follows:

    -   **Organizational Unit:** *Seattle*

    -   **Start Location:** *Organization Unit Address*

    -   **End Location:** *Organizational Unit Address*

9.  Save your changes and close the Resource record.

10. Repeat steps 1 – 9 to define organizational unit, characteristic, and
    category information for the following **Doctors**:

    -   *Allison Dickson*

    -   *Ashley Chinn*

    -   *Bernadette Foley*

11. Navigate to resources and open the **Cheri Castaneda** resource.

12. Locate the **Resource Skills** sub-grid, select the more commands button,
    can choose **Add Bookable Resource Characteristic.**

13. Configure the Bookable Resource Characteristic as follows:

    -   **Characteristic:** *Consultation*

    -   **Rating Value:** *Proficient*

14. Click **Save.**

15. Locate the **Resource Categories** sub-grid, select the more commands
    button, can choose **Add Bookable Resource Category**.

16. Select **Patient Consultant** for the **Resource Category.**

17. Click **Save.**

18. Select the Scheduling tab, and configure the scheduling as follows:

    -   **Organizational Unit:** *Seattle*

    -   **Start Location:** *Organization Unit Address*

    -   **End Location:** *Organizational Unit Address*

19. Save your changes and close the Resource record.

20. Repeat steps 11 – 19 to define organizational unit, characteristic, and
    category information for the following **Patient Consultants**:

    -   *Christal Robles*

    -   *Christie Dawson*

    -   *Clarence Desimone*

### Task 7 – Create a Consultation Work Order Type

Now that we have defined and configured the resources as needed, the final step
is to ensure that we can schedule these items together as a group. To accomplish
this, we will be doing the following:

-   Creating a consultation work order type.

-   Defining a Resource Requirement Group template called consultation.

-   Defining an incident type called consultation.

-   Associating the consultation incident type with the Consultation resource
    requirement group.

Create the Consultation Work Order Type as follows:

1.  In the Site Map button on in the bottom left corner, select **Settings** and
    navigate to **Work Order Types** in the left menu.

2.  Click the **New** button to add a new Work Order Type.

3.  Configure the Work Order Type as follows:

    - **Name:** Consultation

    - **Incident Required:** No

    - **Taxable:** No

    - **Price List:** Default Price List

4.  Click **Save and Close.**

### Task 8 – Create a Resource Group Template called Consultation

1.  Click the down arrow next to **Dynamics 365** in the top menu and select
    **Resource Scheduling.**

2.  In the bottom left corner, open the Site Map and select **Settings.**

3.  In the left menu, select **Requirement Group Templates** and click the
    **New** Button.

4.  In the **Name** field, enter **New Patient Consultation**.

5.  Click the **Save** button to leave the requirement record open.

6.  In the subgrid, select **New Patient Consultation**, click the
    **+Requirement** button.

7.  Replace the name of the Requirement with **Consultation Room**.

8.  Click the **Duplicate Requirement** button and replace the name with
    **Patient Consultant**.

9.  Click the **Duplicate Requirement** button and replace the name with
    **Doctor**.

10. In the Duration field for the **New Patient Consultation**, set the Duration
    to **2 Hours**.

11. In the **Part of the Same** field, select **Organizational Unit**.

12. Select the **Consultation Room** requirement. Click the **Open Form**
    button.

13. Set the **Resource type** to **Facility**.

14. Locate the **Skills** sub-grid, select the more commands button, can choose
    **Add New Requirement Characteristic.**

15. Configure the Requirement Characteristic as follows:

    -   **Characteristic:** *Consultation*

    -   **Rating Value:** *Familiar*

16. Click **Save**

17. Locate the **Resource Categories** sub-grid, select the more commands
    button, can choose **Add Requirement Resource Category**.

18. Select **Consultation Room** for the **Resource Category.**

19. Click **Save and Close**.

20. Select the **Scheduling** tab, set the **work location** to **Location
    Agnostic.**

21. Save your changes and close the Consultation Room Requirement. Return to the
    **New Patient Consultation** Requirement Group record.

22. Select the **Patient Consultant** requirement.

23. Click the **Resource Categories**, and select **Patient Consultant**

24. Click the **Characteristics** field, and select **Consultation**

25. Select the **Doctor** requirement.

26. Click the **Resource Categories**, and **select Doctor**

27. Click the **Characteristics** field, and select **Consultation.** Then
    **Save** the record.

Task 9 – Create an Incident Type that uses the Requirement Group

1.  Click the down arrow next to **Dynamics 365** in the top menu. Open the
    **Field Service** application. In the bottom left hand corner, use the Site
    Map to open **Settings.**

2.  In the left menu, locate **Incident Types** and click the **New** button to
    create a new Incident type.

3.  Enter **Patient Consultation** for the Name.

4.  Select the **Details** tab and configure the Incident details as noted.

    1.  **Default Work Order Type:** *Consultation*

    2.  **Estimated Duration:** *2 Hours*

5.  Click the **Save** button to save the Incident Type and Leave it open.

6.  Select the **Related** tab, from the menu that appears, select **Requirement
    Groups**.

7.  Click the **Add New Incident Type Requirement Group** button.

8.  Enter **Patient Consultation** into the **Name** field.

9.  Select the **New Patient Consultation** Requirement Group.

10. Save your changes and close the Patient Consultation Incident Type.

Task 10 – Configure the Schedule Board

1.  Open the Site Map in the bottom left corner and navigate to **Service**.

2.  Select the **Schedule Board** to open it.

3.  Click on the gear icon to access the Schedule Board settings. Scroll down
    and expand the **Requirements Panel**.

4.  Configure as follows:

    -   **View Type:** *Requirement Group Views*

    -   **Title:** *Unscheduled Requirement Groups*

    -   **View:** *Active Requirement Groups*

5.  Select the add new **(+)** panel button to place the Requirement Group View.
    Click the Apply button.

Exercise 4 - Create a new work order using an incident type
=============================

Out-of-the-box, Dynamics 365 for Field Service has the work order entity enabled
for use with the Resource Scheduling feature. In this task, we will be creating
a new work order that we can schedule using the application.

### Task 1 – Create a New Work Order from an Incident Type

1.  In **Dynamics 365**, click the arrow next to the **Dynamics 365** text, and
    select **Field Service**.

2.  In the left column, select **Work Orders**.

3.  Click the **New** button.

4.  Configure the work order as follows:

    -   **Service Account:** *Adventure Works (Sample)*

    -   **Work Order Type:** *Inspection*

    -   **Taxable:** *No*

    -   **Primary Incident Type:** *MRI Inspection*

5.  Click the Settings tab, and Configure as follows:

    -   **Priority:** *Moderate*

    -   **Service Territory:** *WA*

    -   **Time from Promised:** *Today \@ 1:00 PM*

    -   **Time to Promised:** *Today \@ 3:00 PM*

6.  **Save and Close** the work order

Exercise 5 - Schedule the work order using the schedule board
=============================================

Universal Resource Scheduling provides several items that can be used to assist
in scheduling resources for specific items. The two primary components that are
used are the Schedule Board and the Schedule Assistant. The Schedule Board
provides the ability to manually schedule items, and the assistant offers
suggestions on resources based on factors like location, skills, and
availability. In this task we will examine how you can use the schedule board to
schedule items and a high level.

### Task 1 – Schedule the Work Order you just created

1.  In the left column, open the **Schedule Board**.

2.  The Schedule Board provides several options that can be used to schedule
    items, such as a filter, and a map view.

3.  Expand the **Booking Requirements** pane.

4.  Select **Unscheduled work orders**.

5.  Locate the **work order** for Adventure Works (Sample) that you created in a
    previous task. Drag it to Allison Dickson on the schedule board. *Notice
    that it the text will appear red until you find a time that falls within the
    time window promised.*

6.  Release the mouse button and the item will be placed on the schedule board.

7.  Locate and select the work order for **Fourth Coffee (Sample)** under
    **Unscheduled work orders.** Click **Find Availability**.

8.  Dynamics 365 will analyze the requirements needed for this item and will
    factor in other items such as any skills required, work order & resource
    locations, and resource availability to create a list of suggested resources
    that would be able to work on this item.

9.  As you hover over the available time block for **Van Amundson**, a **Book**
    icon will appear. Click the **Book** icon to schedule Van for this work
    order.

10. Click the **Exit Search** Icon to return to the Schedule Board.

### Task 2 – Schedule a Work Order using the Map View

Another way that items can be scheduled is by using the map view on the Schedule
Board. When you select the map view, resources will be color coded. Any
unscheduled items will appear on the map with a question mark. You can schedule
these items by dragging them to a specific resource that you want to assign it
to.

As you start assigning items to resources, the item will change to the color of
the resource selected. Additionally, the map will begin to plot a route for the
resource based on the location of the work orders assigned to them.

Additional items like traffic and road maps can be overlaid on the map to assist
in scheduling.

1.  On the Schedule Board, click the **Map View**.

2.  To see Traffic, click the **Show Traffic** Icon.

3.  Locate an item on the map that is unscheduled. *(It will appear with a Red
    Exclamation Point)* Drag the item to open time slot on Allison Dickson’s
    schedule right before the work order you scheduled for her previously.
    Notice that a booking is created, and the Requirement has been changed to
    Allison’s pin color.

4.  Locate another unscheduled item on the map.

5.  Hover over the unscheduled item. On the Tooltip that appears click **Find
    Availability**.

6.  Dynamics 365 will analyze the requirements needed for this item and will
    factor in other items such as any skills required, work order & resource
    locations, and resource availability to create a list of suggested resources
    that would be able to work on this item.

7.  As you hover over the available time block for **Any resource with
    availability**, a **Book** icon will appear. Click the **Book** icon to
    schedule the resource for this work order.

Exercise 6 – Rescheduling and Rebooking Items
============================================

Often, something happens that requires an item to either be rebooked all
together at a different day and time or have maybe it just required that a
different resource be substituted for the item.

### Task 1 – Manual reschedule an Item

1.  On the schedule board, click the **filter** tab on the **Filter and Map**
    View.

2.  In **Territories** filter control, select **WA**. Ensure all other filter
    criteria is left blank and click the **Search** button.

3.  Locate the Fan not working work order for Joseph Gonsalves.

4.  **Right-click** the work order and from the menu that appears, select
    **Rebook**.

5.  The **Schedule Assistant** will open. You should be presented with between 4
    and 7 resources who have availability.

6.  Click the availability block for Efrain Schreiner. In the **Create Resource
    Booking** screen accept the defaults and click **Rebook & Close**.

7.  Locate the hard disk boot failure work order for Joseph Gonsalves.

8.  **Right-Click** the work order and from the menu that appears, select
    **substitute resource**, **Find substitution**.

9.  The **Schedule Assistant** will open. You may only be presented with 1 or 2
    resources.

10. Hover over the availability block that is presented for Simon Raley. Click
    **Substitute**.

11. The booking will be reassigned from Joseph to Simon.

Exercise 7 – Scheduling Multiple Resources
======================================

### Task 1 – Schedule Resource Pools and Requirement Groups

1.  Under the **Scheduling** section in the left menu, navigate to **Work
    Orders**.

2.  Click the New button to create a new work order and configure the new work
    order as follows:

    -   **Service Account:** *Blue Yonder Airlines*

    -   **Billing Account:** *Blue Yonder Airlines*

    -   **Work Order Type:** *Inspection*

    -   **Taxable:** *No*

3.  Click the **Save and Close** button

4.  Click the **New** button to create a new work order and configure the work
    order as follows:

    -   **Service Account:** *City Power & Light (sample)*

    -   **Primary Incident type:** *Consultation*

5.  Click the **Save and Close** button

6.  Use the left menu to navigate to the **Schedule Board**.

7.  In the **Search Resources** field, enter **Consultation**. The
    **Consultation Rooms resource pool will be displayed**.

8.  In the **Unscheduled Work Orders** tab locate the resource requirement for
    Blue Yonder Airlines and drag it and place it into an open slot for the
    resource pool.

9.  With your mouse hover over the **Consultation Rooms** resource pool,
    Right-click and select **View pool in split view**.

10. Each of the Screen Rooms will be presented as part of the resource pool.

11. Drag the **Scheduled item** and place it on the **Screen Room A** facility
    record.

12. In the **Unscheduled Requirement Groups** panel, select requirement group
    that was just created when you created the work order, and select **Find
    Availability**

13. You will be presented with multiple combinations of **Patient Consultants**,
    **Doctors**, and **Consultation Rooms**.

14. Select the suggestion you want to book and click the **Book and Exit**
    button.
