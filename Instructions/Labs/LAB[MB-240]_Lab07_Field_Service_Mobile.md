---
lab:
    title: 'Lab: Configure mobile'
    module: 'Module 8: Field Service Mobile'
---

Module 8 - Field Service Mobile
=====================
## Practice Lab 7 - Configure mobile

## Scenario

World Wide Industries (WWI) provides IT and networking services to their
customers. Their services range from phone system and network installations to
phone and telephoning systems and security system installations. They are going
to be leveraging Dynamics 365 for Field Service for installation and servicing
of these systems for their customers. You’re are the system implementer that has
been tasked with configuring the application to support the roll-out of the
application. You will be adding and configuring some products that can be
installed as well as setting up some skills and characteristic that will be used
as part of the implementation.

WWI Dispatches its technicians to work on items in the field. They plan on
leveraging the Field Service Mobile application to manage the daily servicing of
these customers while technicians are working in the Field. You have been tasked
with deploying and configuring the mobile application to meet their specific
needs.

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

Exercise 1 - Download and install the Mobile Field Service mobile solution.
===========================================================================

**Before you Begin:** You will need administrator permissions to install the
Mobile Dynamics 365 Woodford mobile solution for field service capabilities in
Dynamics 365. You also need to use Internet Explorer with Silverlight or
Firefox.

## Task 1 - Download and install the Mobile Field Service mobile solution

Before beginning this task, navigate to the following URL to download and save the Woodford mobile solution from the Resco site to your computer: <https://www.resco.net/mobilecrm/woodford.html> 

(You should download and install the solution that matches the version of the Field Service Mobile application you are running.)

**Note:** The Solution contains the editor that can be launched from
the Dynamics 365 Solution. It is also recommended that you download the
Standalone editor. It is a desktop editor that can be executed from your
desktop and is not dependent on any other technology. Click the Install
Button.

1.  Locate the Standalone Application section and click the Install button.

2.  Switch to your Dynamics 365 Instance where **Field Service** is installed.

3.  Navigate to **Settings** > **Solutions**.

4.  From the **Solutions** area, click the **Import** button.

5.  Locate the Woodford Solution you downloaded earlier, click **Next**,
    finally, click the **Import** button.

6.  After the solution is imported, you should see the **Woodford** solution
    listed on the **Settings** menu. To verify this, go to **Settings**, and
    then click **Woodford**. **Important:** If you don’t see **Woodford** under
    the **Settings** menu, refresh the page.

7.  Locate the Standalone Editor that you downloaded. If the Standalone
    application is not started. Launch the application. If prompted to Increase
    Quota, set the quota to **100MB**, and then click **OK.**

8.  In the **Update available** dialog box, when you're prompted about an
    available update, click **Later**. (**IMPORTANT:** *Do not update even if
    one is available)*

9.  If prompted to Install Silverlight, Right click on the app and click
    **Install**.

10. Provide your credentials again.

11. Provide your credentials and click **OK**.

Exercise 2 - Import the Field Service mobile project template into the Woodford Solution
=========================================================================================

After the Woodford solution is installed, you’ll need to download a template
that will help you configure the mobile app. The template is required if you are
using the Woodford solution. The template contains all customizations for the
field service mobile app. You can use it to add, remove, and change fields,
entities, views, and forms.

## Task 1 - Import the Field Service mobile project template into the Woodford Solution

1.  Download and save the temple file.

    -   If you are on December 2016 update for Microsoft Dynamics 365 (online),
        use this [mobile project
        template](https://go.microsoft.com/fwlink/p/?linkid=836310)

    -   If you are on Microsoft Dynamics 365, use this [mobile project
        template](http://go.microsoft.com/fwlink/p/?LinkId=808250)

2.  Go into the editor, click **Import**, and then import the mobile project
    template file that you saved in Step 1.

3.  In the **Add Mobile Project** dialog box do this:

    -   For **Type**, select **Standard User**.

    -   Name the **template**.

    -   Set the **Priority** to 10

4.  For **Roles**, select the roles you want this mobile template to apply to,
    and then click **OK**. A user who signs in and has a role that matches the
    role you select here, will inherit this configuration on their mobile app.

5.  To publish the template file, on the **Mobile Project** tab, click **Edit**.

6.  Click OK.

7.  On the next screen, click **Publish All.**

## Task 2 - Customize the Field Service Mobile App.

Now that you have created your environment, it is time to start customizing the
application. First, we will customize the home screen:

1.  In the Wordford customization application, click on the **Home** button.

2.  Locate the **Case** entity from the available Item list on the right and
    drag it under Product on the Home section

3.  Click **Save**.

4.  Navigate to **Color Theme** \> and click the **Title Background** next to
    the word Home item in the theme section.

5.  Select any color that you would like and then click **Done**

6.  Click the Tab Background next to the General Icon in the lower right. Select
    any color that you would like and then click **Done**.

7.  Click **Save**.

8.  In the left side of the application locate the click on the Case entity.

9.  Expand the Case entity and select Fields. Select the following fields:

	-   Entitlement

	-   Parent Case

	-   Serial Number

	-   Service Level

10.  Click **Save**.

11.  On the **Case** entity, select **Views**, then click the **Clone** button.

12.  Enter **High Priority Cases** for the name, and click **OK**

13.  Click the **Edit Filter** button.

14.  Expand the Case and choose **Add Condition**.

15.  Set the Condition to **Priority** > **Equals** > **High**.

16.  Click **Case** again and Add another Condition

17.  Set the Condition to **Owner** > **Equals Current user**.

18.  Click **Save and Close**.

19.  Select the Customer Field under Case Title.

20.  In the command bar, click the **Buttons** Icon.

21.  Under **Available Commands**, click **Email**, the click **Add**

22.  Click **Save and Close**.

23.  Click **Save and Close** to save the View

24.  Under **Case**, select **Forms**

25.  Click **Edit**.

26.  Drag the **Serial Number** Field below **Status Reason**

27. Click **Save and Close**

28. Click the **Validate Button**

29. Click **Publish All**

30. Open the Field Service Mobile application and Verify your Changes.

Exercise 3 - Customize the Work Order Service Tasks Entity
=======================================

Many times, you will need to not only customize the mobile project, but you may
also need make some additional changes in the dynamics 365 application to
support functionality. In the following task we will customize the Work Order
Service Tasks entity in Dynamics 365 and the mobile project to allow us to use
check boxes to complete work order service tasks.

### Task 1 – Task List Customizations

1.  In your Dynamics 365 Organization, navigate to **Settings** >
    **Customizations** > **Customize the System**.

2.  In the Default Solution, expand entities, **Work Order Service Tasks**, and
    click **Fields**

3.  Click **New** to create a new field

4.  Configure the new field as follows:

    -   **Display Name:** Completed

    -   **Data Type:** Two Options

5.  Click **Save** and **Close**

6.  Click **Publish All Customizations**

1.  Click **Save and Close**.

2.  Select the Customer Field under Case Title.

3.  In the command bar, click the **Buttons** Icon.

4.  Under **Available Commands**, click **Email**, the click **Add**

5.  Click **Save and Close**.

6.  Click **Save and Close** to save the View

7.  Under **Case**, select **Forms**

8.  Click **Edit**.

9.  Drag the **Serial Number** Field below **Status Reason**

10. Click **Save and Close**

11. Click the **Validate Button**

12. Click **Publish All**

13. Open the Field Service Mobile application and Verify your Changes.

### Task 2 - Customize the Work Order Service Tasks entity

1.  If the Woodford customization tool is still open, you will need to close and
    restart the editor.

2.  Select the project you created earlier and click **edit**.

3.  Expand **Work Order Service Task**, select **Fields**, check the
    **Completed** Field

4.  Click **Save**

5.  Navigate to **Views**, and open the **ServiceTaskList** view

6.  In the ribbon at the top, click the **Select Fields** button.

7.  Enable the **completed** field, and click **OK**

8.  In the Properties section, change the view height to 60

9.  Drag the **Completed** below the Name field.

10. In the Properties section, send the **Kind** field to **Text-Edit**

11. Click **Save and Close**

### Task 3 - Use the updated view with the service task list

1.  Navigate to **Views**, and open the **ServiceTaskList** view

2.  Under the **Associated** views, deselect **DetailedServiceTaskList**.

3.  Click **Save and Close**

4.  **Publish**

### Task 4 - Add colors to Work Order Products

1.  In the Woodford customization application, open your **Field Service
    Mobile** Project.

2.  Navigate to **Work Order Products**, and open the **DetailedProductList**
    view

3.  On the Ribbon, click **Select Fields**, select the **Line Status** field

4.  Locate the **Description** field, double click the field, and change it to
    **Line Status**

5.  On the **Ribbon**, click **Clone Row**

6.  In the Colors Field select a color that works for you

7.  Rename the Row to **Estimated**

8.  Create another **Cloned Row**

9.  In the **Colors** Field, select a different color

10. Rename the Row to **Used**

11. In the Ribbon, click the **Row Script** Button

12. Click the **Add** Condition button

	- Configure the condition as follows: **Entity** – **msdyn_linestatus** – **equals** – **estimated**

13. Click **Add Step**

    - Configure the Step as follows: **TemplateIndex** – **Assign** – **Estimated** 
   

14. Click the **Add If/Otherwise** button, configure the rest of the Row Script
    as shown in the Image below:

15. Click **Save and Close**

16. Navigate to the **Work Order** Form, double click the **Products** tab, and
    select the color-coded view you just did

17. Click **Save and Close**

18. **Publish** your Project
