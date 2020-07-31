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

Exercise 2 – Configure supporting resources, roles, and skills
===========================

### Task 1 – Create three resource categories

Before we start making the resource facilities, pools, and requirement groups
that will be used to support the scheduling scenario, we what to ensure that we
have the necessary supporting components defined that will be used to schedule.

To make it as easy as possible we are going to add three resource categories
that can be easily used to identify consultation rooms, patient consultants, and
Doctors.

1.  With the **Field Service** application open, click the Sitemap in the
    bottom left corner and select **Resources.**

2.  Open **Categories** in the left menu.

3.  Click the **New** button to create a new Resource Category.

4.  Enter **Consultation Room** into the Name field and select **Save and
    Close.**

5.  Click the **New** button to create another new Resource Category.

6.  Enter **[your prefix ex. mollyc]+ Patient Consultant** into the name field and select **Save and
    Close.**

7.  Click the **New** button to create the last new Resource Category.

8.  Enter **[your prefix ex. mollyc]+ Doctor** into the name field and select **Save and Close**.

### Task 2 – Create a Consultation Characteristic

Some doctors may be able to do consultations, and some may not. To ensure that
we can identify the doctors that are able to perform consultations, we are going
to add a new resource characteristic called Consultation. This characteristic
will be added to any resource that could be used in a consultation.

1.  While you are in **Resources** section, click **Characteristics** in the
    left menu. (make sure the view is set to **Resource Characteristics**

2.  Click the **New** button to define a **Characteristic**.  Ensure the form is set to **Information**

3.  Enter **[your prefix ex. mollyc]+ Consultation** into the Name field. (If prompted to create a new
    Characteristic, press new and create the Characteristic before assigning it
    as a Bookable Resource Characteristic.  Set the type to **Skill**)

4.  Enter your user record as the Resource.

5.  **Save and close.**

### Task 3 – Configure Resource Working Hours

One factor that goes a long way in ensuring that all resources that will be
working together on projects or as part of a pool have the same working hours.
Work hours can be defined for up to 25 resources at one time by creating a work
hours template. A work hours template must be based on another resource’s
working hours.

We will start by defining the working hours for a single resource. We will use
that resource to create the Work Hours Template.

1.  While you are in **Resources**, click **Resources** in the left menu.

2.  Locate and select the resource record for your user.

3.  On the **command bar** at the top, click the **Show Work Hours** button.
    *(Note: you may need to allow pop-up windows if you are running a popup
    blocker.)*

4.  Select the **+New** drop-down and select **Working hours**.

5.  Change *repeat* to **Every Week**.

6.  When the weekly schedule is displayed, make sure **Mo thru Fr** are checked.

7.  Verify the Work Hours are set to **8:00 AM** to **5:00 PM** and click
    **Save**

8. Verify that the new schedule is being applied moving forward and **Close**
    the **Work Hours window.**

11. In the left menu, click on **Workhour Templates.**

12. Click the **New** button to define a new template.

13. Define the template as follows:

    - **Name:** *[your prefix ex. mollyc]+ Standard Hours*

    - **Template Resource:** *your user*

14. Click **Save and Close.**

Exercise 4 - Create a new work order using an incident type
=============================

Out-of-the-box, Dynamics 365 for Field Service has the work order entity enabled
for use with the Resource Scheduling feature. In this task, we will be creating
a new work order that we can schedule using the application.

### Task 1 – Create a New Work Order from an Incident Type

1.  In **Dynamics 365**, click the arrow next to the **Dynamics 365** text, and
    select **Field Service**.

2.  From the sitemap in the bottom left corner, select **Service**. In the left column, select **Work Orders**.

3.  Click the **New** button.

4.  Configure the work order as follows:

    -   **Service Account:** *[your prefix ex. mollyc]+ Account* (should have been created earlier.  If not, create a new Service Account with name *[your prefix ex. mollyc]+ Account*)

    -   **Work Order Type:** *Inspection*

    -   **Taxable:** *No*

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

5.  Locate the **work order** for [your prefix ex. mollyc]+ Account. Drag it to your user on the schedule board.

6.  Release the mouse button and the item will be placed on the schedule board.

7.  Locate and select the work order for **[your prefix ex. mollyc]+ Coho Winery** under
    **Unscheduled work orders.** Click **Find Availability**.

8.  Dynamics 365 will analyze the requirements needed for this item and will
    factor in other items such as any skills required, work order & resource
    locations, and resource availability to create a list of suggested resources
    that would be able to work on this item.

9.  As you hover over the available time block for **your user**, a **Book**
    icon will appear. Click the **Book** icon to schedule Van for this work
    order.

10. Click the **Exit Search** Icon to return to the Schedule Board.
