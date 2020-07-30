---
lab:
    title: 'Lab: Configure Universal Resource Scheduling'
    module: 'Module 9: Universal Resource Scheduling'
---

Module 9 - Universal Resource Scheduling
=====================
## Practice Lab 8 - Universal Resource Scheduling

## Scenario

Worldwide Industries (WWI) provides IT and networking services to their
customers. Their services range from phone system and network installations to
telephoning systems and security system installations. They are going to be
leveraging Dynamics 365 for Field Service for installation and servicing of
these systems for their customers. You are the system implementor that has been
tasked with configuring the application to support the rollout of the
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
======================================

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
  
Exercise 2 – Map Configuration  
==============================
 
### Task 1 - Enable Bing Maps to use with Resource Scheduling 

To ensure that you are able to take full advantage of the full scheduling and
mapping capabilities available with Field Service, you need to ensure that it is
configured to use a mapping provider.  Bings Maps is the default map provider,
but additional providers could be enabled.  We will be using Bing Maps. 

1.  In **Dynamics 365**, click the arrow next to the **Dynamics 365** text, and
    select **Resource Scheduling**.   

2.  Click the **Site Map** icon in the bottom left corner.  Click on **Settings.**  From the menu that
    appears, select **Administration**.   

3.  Select **Scheduling Parameters**. 

4.  Locate the **Connect to Maps** field and set it to **Yes**. 

5.  **Save and Close** the settings.   

Exercise 3 – Resource Configuration 
====================================

Before you can start scheduling items and assigning them to specific resources
in your organization, you need to first create bookable resources in the
application. A bookable resource could be an internal user, an external contact
or account, or a piece of equipment. When you define a bookable resource, you
can also provide details such as skills they have, where they start and end
their day and so on.

In this first task we will be creating a bookable resource record for a new
Contact Record that we will be creating.

### Task 1 - Create a Bookable Resource for your user record

Note: If you have already created a bookable resource for your user, skip to Exercise 4.

1.  Expand the **Sitemap** and select **Resource Scheduling**.  Select **Resources** under **Scheduling**

2.  Click **New** button to create a new **Bookable Resource**.

3.  Configure the new **Bookable Resource** record as follows:

    - **Resource Type:** *User*

    - **User:** *your user (example alans or Alan Steiner)*

    - **Time Zone:** Leave the default value in the Time Zone Field.

4.  Select the **Scheduling** tab.

    - Set the **Organizational Unit** field to **Seattle.**

    - In the **Start Location** field, select **Resource Address**.

    - In the **End Location** field, select **Resource Address**.

5.  Select the **Field Service** tab.

    - Set the **Hourly Rate** field to **175**.

6.  **Save** the bookable resource record and leave it open.

7.  Locate the **Characteristics** sub-grid, click **Add New Bookable Resource
    Characteristic**

8.  Configure as follows:

    -   **Characteristic:** *Building Security*

    -   **Rating Value**: *Proficient*

    -   Click **Save and Close** on the characteristic record.

9.  Select **Add New Bookable Resource Characteristic** Again

10. Configure as follows:

    - **Characteristic:** *CISM*

    - **Rating Value**: *Proficient*

    - Click **Save and Close** on the characteristic record.

11. Select **Add New Bookable Resource Characteristic** Again

12. Configure as follows:

    - **Characteristic:** *CISSP*

    - **Rating Value**: *Familiar*

    - Click **Save and Close** on the characteristic record.

13. Select **Add New Bookable Resource Category Assn**

14. Configure as follows:

    - **Resource Category:** *Installation Specialist*

    - Click **Save and Close** on the Category record.

15. Select **Add New Bookable Resource Category Assn** again.

16. Configure as follows:

    - **Resource Category:** *Security Analyst*

    - Click **Save and Close** on the Category record.

17. **Save and Close** the bookable resource record**.**

18. Select the **Related** tab.

19. From the menu that appears, select **Resource Territories**.

20. Click the **Add New Resource Territory** button.

    - In the **Territory Lookup** field, select **WA**.

    - Select the **Save and Close** button.

21. Select the **Show Work Hours** button. A new window will open.

    - In the Calendar view, click the **Set Up** drop-down button.

    - From the menu that appears, choose **New Weekly Schedule**.

    - Leave the working hours as **Are the same for each day** and click the
        **Set Work Hours** Hyperlink.

    - Ensure the Work Hours are set to **8:00 AM** to **5:00 PM** and click
        **OK**

    - Uncheck **Sun** and **Sat**.

    - Click **Save and Close**.

22. Verify that the schedule is showing 8:00 AM to 5:00 PM – Monday – Friday
    from today forward.

23. Close the Work Hours Calendar window.


Exercise 6 – Enable the Time Off Request Entity for URS
======================================

There are two main entities that are used for scheduling an item using URS. The
Resource Requirement entity and the Bookable Resource Booking entity. The
Resource Requirement entity is used to define what is needed to schedule an
item. Typically, the Resource Requirement includes things like the start and end
time, duration, skills required and so on. Once a resource that meets the
requirements is found, a Bookable Resource Booking is created and displayed on
the schedule board.

For a Time Off Request to appear on the schedule board, a Resource Requirement
must first exist, and then a Bookable Resource Booking can be created. To
achieve this, the Time Off Request entity needs a relationship with both the
Resource Requirement and Bookable Resource Booking. This can be accomplished by
enabling the Time Off Request entity for URS.

**To accomplish this, we will be doing the following:**

-   Enabling the Time Off Request entity for URS.

-   Configuring mapping for the Time Off Request entity and the Resource
    Requirement and Bookable Resource Booking entities.

### Task 1 - Enable the Time Off Request for URS

1.  In **Dynamics 365**, select the arrow to open the dropdown menu of apps.

2.  Select the **Resource Scheduling** App.

3.  Click the **Site Map** icon at the bottom left corner. Select **Settings.**

4.  Select **Administration** in the left menu and then open **Enable Resource
    Scheduling for Entities.**

5.  Configure as follows:

    -   **Add Entity:** *Time Off Request*

    -   **Booking Relationship:** *Create New Relationship*

    -   **Requirement Relationship:** *Create New Relationship*.

6.  Click **Publish Customization**.

7.  Double click *Time Off Requests* under **Enabled Entities**

8.  Under Settings for the Time Off Request entity, configure as follows:

    -   **Default Booking Duration:** *1 Hour*

    -   **Disable Requirement Auto Creation:** *Yes*

9.  Under Attribute Mapping, configure as follows:

    -   **From Date:** *Start Time*

    -   **To Date:** *End Time*

    -   **Duration:** *Duration (Deprecated)*

10.  Close the **Time Off Request** window.

### Task 2 - Create a Workflow

Now that the Time Off Request entity has been enabled for URS, we need to make
sure that both the necessary Resource Requirement and Corresponding Bookable
Resource Booking are automatically created so they can be populated on the
schedule board. To accomplish this, we will be creating a workflow that will do
the following:

-   Create a Resource Requirement record with the necessary data populated from the Time Off Request.

-   Create a Bookable Resource Booking associated with the Resource Requirement
    that is assigned to the Resource that submitted the Time Off Request.

Next, we'll configure the workflow.

1.  In the **Default Solution**, locate **Processes**, click the **New** button
    to add a new process.

2.  Configure the new process as follows:

    -   **Process Name:** *Schedule Time Off*

    -   **Category:** *Workflow*

    -   **Entity:** *Time Off Request*

3.  Click **OK**

4.  Under **Options for Automatic Processes**, set the **Scope** to
    **Organization**. Ensure that **Start when** is set to **Record is
    Created**.

5.  In the **Workflow Designer** click the **Add Step** button, from the menu
    that appears, select **Create Record**.

6.  In the **Description** field, enter **Create a Resource Requirement for the
    Time Off Request**.

7.  Select **Resource Requirement** and click **Set Properties**.

8.  Configure the Resource Requirement as follows:

	-   **Name:** {Name(Time Off Request)}

	-   **From Date: {**Start Time(Time Off Request)}

	-   **To Date:** {End Time(Time Off Request)}

	-   **Duration:** {Duration(Time Off Request)}

	-   **Status:** Active

	-   **Time Off Request:** {Time Off Request(Time Off Request)}

	-   **Allocation Method:** None

9.  Click **Save and Close**

10.  In the **Workflow Designer** click the **Add Step** button, from the menu
    that appears, select **Create Record**.

11.  In the **Description** field, enter **Schedule the Time Off Request**.

12.  Select **Bookable Resource Booking** and click **Set Properties**.

13. Configure the Bookable Resource Booking as follows:

	-   **Name:** *{Name(Time Off Request)}*

	-   **Start Time:** *{Start Time(Time Off Request)}*

	-   **End Time:** *{End Time(Time Off Request)}*

	-   **Duration:** *{Duration(Time Off Request)}*

	-   **Resource:** *{Resource(Time Off Request)}*

	-   **Booking Status:** *{Time Off Type (Time Off Request)}*

	-   **Resource Requirement:** *{Resource Requirement(Create(Resource
    Requirement))}*

14.  Click **Save and Close**

15.  Your completed workflow should resemble the following image:

16. **Save** and **Activate** the workflow.

Exercise 7 – Defining necessary Time Off Booking Statuses
================================================

Now that everything has been setup and configured in Dynamics 365, we will see
how they all works together. We will add some Time Off statuses to the
application, and then use those statuses to create a Time Off Request that will
be automatically added to the Schedule Board.

**To accomplish this, we will be doing the following:**

-   Adding three new Time Off Booking Statuses.

    -   Doctor appointment

    -   Vacation

    -   Seminar

-   Creating a Time Off Request record for vacation.

-   Viewing the Time Off Request on the Schedule Board.

### Task 1 – Add Time Off booking statuses

1.  Open the **Resource Scheduling** app by expanding the menu next to “Dynamics
    365.”

2.  Click the **Site Map** icon and locate **Settings**. Click **Booking
    Statuses**

3.  Click the **New** button

4.  Configure the Booking Status as follows:

    -   **Name:** *Dr. Appointment*

    -   **Time Off Status:** *Yes*

5.  Click **Save and Close**

6.  Click the **New** button, and configure the Booking Status as follows:

    -   **Name**: *Vacation*

    -   **Time Off Status:** Yes

7.  Click **Save and Close**

8.  Click the **New** button, and configure the Booking Status as follows:

    -   **Name:** *Seminar*

    -   **Time Off Status:** Yes

9.  Click **Save and Close**

Exercise 8 – Testing Functionality
====================================

### Task 1 - Create a Time Off Request

1.  Switch to the **Field Service** app.

2.  In the left menu, under **Scheduling**, select **Time Off Request**.

3.  Click the **New** Button

4.  Configure the Time Off Request as follows:

    - **Resource:** *Your Resource Record*

    - **Start Time:** *Tomorrow at 8:00 AM*

    - **End Time:** *Tomorrow at 5:00 PM*

    - **Time Off Type:** *Vacation*

5.  Click the **Save and Close** button.

6.  Click the **Site Map** Icon, under **work order & Scheduling**, click the
    **Schedule Board**.

7.  Scroll to tomorrow’s date.

8.  Notice the **Time Off Request** appears.
