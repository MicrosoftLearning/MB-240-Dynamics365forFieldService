Practice Lab 10 - Customize the Schedule Board
======================================

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
====================================================

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

    1.  **Note:** If you have already selected your trial in a previous lab
        exercise, you will be taken to the D365 Administration Center. If so,
        select the **Open** circled arrow button beside “Contoso Production.”

6.  When viewing tiles of all available applications, click on “Field Service”
    to open your Dynamics 365 instance to the Field Service application. You
    have now entered your Dynamics 365 production environment and are ready to
    explore the Field Service app.

Exercise 2 – Customize the Schedule Board
=========================================

As a dispatcher, you spend a lot of time scheduling for the multiple territories
that your organizations support. One scenario that comes up often, is the need
to schedule for Washington Customer. Since the board will be focused on
Washington customers, you would like to ensure the following:

1.  Only open requirements in the Washington Territory are displayed in the
    Requirements panel.

2.  Only open requirements in the Washington Territory are shown on the Map
    View.

3.  The view is only showing Washington Resources.

4.  When a resource is selected, the details view includes the territory.

### Task 1 - Customize the Resource Requirement views

1.  In Dynamics 365, select the gear icon in the top menu. Open **Advanced
    Settings.**

2.  Select the dropdown menu next to “Settings” and open **Customizations.**

3.  Under **Entities**, expand the **Resource Requirement** entity, and select
    **views**.

4.  Locate and open the **Unscheduled Work Order Requirements** view.

5.  Click **Save As** and save the view as **Unscheduled WA Work Order
    Requirements**.

6.  Select the **Edit Filter Criteria** button.

7.  Locate and click in the **Select** field below the System Status – Equals –
    Open Unscheduled.

8.  Configure the items as follows:

    -   **Field:** *Service Territory*

    -   **Operator:** *Equals*

    -   **Value:** *WA*

9.  After you have defined the criteria, click **OK**.

10. **Save and Close** the Unscheduled WA Work Order Requirements View.

11. Locate and open the **Active Resource Requirements** view

12. Click **Save As** to save the view as **Active Resource Requirements (with
    Territory)**

13. Click the **Add Columns** button.

14. From the list, select the **Territory** field, and click **OK**.

15. Ensure the Territory field has a green boarder around it, and using the
    arrows position the Territory field in between the Duration and Priority
    fields.

16. **Save and Close** the **Active Resource Requirements (With Territory
    view)**

17. Click **Publish All Customizations**

### Task 2 - Create and configure the WA Resources schedule board tab

1.  Select the down arrow next to the **Dynamics 365** text in the upper left
    corner.

2.  From the menu that appears, select **Field Service.**

3.  In the left menu, navigate to **Schedule Board** under **Scheduling**
    heading.

4.  Click the Add Tab **(+)** button in the upper right corner of the screen
    nest to initial public view.

5.  In the **Name** field, enter **WA Resources**. Ensure that the **Shared
    with** field is set to **Just Me.**

6.  Under **Map Settings**, set the **Requirement Map Filter View** to
    **Unscheduled WA Work Order Requirements.**

7.  Scroll down and expand the **Schedule Types** tab.

8.  Select the **Work Order** entity. In the **Requirement Details View** field,
    select **Active Resource Requirements (With Territory)**

9.  Scroll down and expand the **Requirement Panels** tab.

10. Configure the new Requirement panel view as follows:

    -   **View Type:** *Requirement Views*

    -   **Title:** *Unscheduled WA Work Orders*

    -   **View:** *Unscheduled WA Work Order requirements*

11. Click the **Add** button to add the Unscheduled WA Work Order Requirements.

12. Check the **Hide default requirement panels**.

13. Click the **Add** button to add the new Schedule Board tab.

14. After the WA Resources tab loads, locate the **Filter** tab on the Filter
    and Map View.

15. In the **Territories** filter control, select WA

16. Ensure all other filter criteria is empty can click **Search**.

17. Locate the **Options** button on the **Filter** tab. Click the options
    button and choose **Save current filters as default**.

18. Switch to the **Initial Public View** tab.

19. Switch back to the **WA Resources** tab.

20. The Requirements panel should only show the **Unscheduled WA Work Orders**
    tab.

21. Select a requirement from the Unscheduled WA Work Orders tab. Notice that it
    displays the Territory in the details section.
