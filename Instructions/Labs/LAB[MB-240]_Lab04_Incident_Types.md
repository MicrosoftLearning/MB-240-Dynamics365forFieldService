Practice Lab 4 - Incident Types
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
==============================

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

Exercise 2 – Create an Incident Type called Printer Installation
================================================================

### Task 1 –Service Task Types to be used with Incidents:

1.  Using the **Sitemap**, select **Service Task Types** under **Work Order**
    settings

2.  Click the **New** button and enter **Clean Printer Assembly** for the Name.

3.  Select **30 Minutes** for the **Estimated Duration.**

4.  Click **Save and Close.**

5.  Repeat Steps 2 – 4 to add each of the following:

    1.  **Replace Toner:** *Duration 15 Minutes*

    2.  **Finial Test:** *Duration 15 Minutes*

### Task 2 –Create a Service Printer Incident Type

1.  Using the **Sitemap**, select **Incident Types** under **Work Order**
    settings.

2.  Click the **New** button and enter **Service Printer** for the Name.

3.  Select the Details tab, and configure as follows:

-   **Copy Incident Items to Agreement:** *Yes*

-   **Default Work Order Type**: *Service Call*.

1.  Click **Save** to save the Incident type and leave it open.

2.  Select the **Service Task** Tab, click the **Add Incident Type Service
    Tasks** button. (If pop ups are blocked, you may need to unblock them)

3.  Enter **Clean Printer Assembly** for the **Name**, select **Clean Printer
    Assembly** as the task type, ensure 30 minutes is set for **Estimated
    Duration**.

4.  Click **Save and Close.**

5.  Click the **Add Incident Type Service Tasks** button again.

6.  Enter **Replace Toner** for the **Name**, select **Replace Toner** as the
    task type, ensure 15 minutes is set for **Estimated Duration**.

7.  Click **Save and Close.**

8.  Click the **Add Incident Type Service Tasks** button one last time.

9.  Enter **Finial Test** for the **Name**, select **Finial Test** as the task
    type, ensure 15 minutes is set for **Estimated Duration**.

10. Click **Save and Close.**

11. Select the **Product** tab

12. Click the **Add New Incident Type Product** button.

13. Configure the Incident Type Product as follows:

    -   **Name:** *Remote Printer*

    -   **Unit:** *Primary Unit*

    -   **Quantity:** *1*

    -   **Product:** *Remote Printer*

14. Click the **Save and Close** button

15. Select the **Services** Tab.

16. Click the **Add New Incident Type Service** button.

17. Configure the new Incident Type Service as follows:

    -   **Name:** *Printer Service Fee*

    -   **Unit:** *Primary Unit*

    -   **Quantity:** *1*

    -   **Product:** *Remote Printer*

18. Click the **Save and Close** Button

19. Select the **Characteristics** tab

20. Click the **Add New Incident Type Characteristics** button

21. Configure the Incident Type Characteristic as follows:

    -   **Characteristic:** *CISM*

    -   **Rating Value:** *Familiar*

22. Click the **Save and Close** button

23. Click the **Add New Incident Type Characteristics** button

24. Configure the Incident Type Characteristic as follows:

    -   **Characteristic:** *Building Security*

    -   **Rating Value:** *Level 2 Security*

25. Click the Save and Close Button

Exercise 3 – Test your Configuration Settings
=============================================

### Task 1 –Create a new Work Order using Service Printer Incident Type:

1.  Using the **Sitemap**, select **Field Service**.

2.  Under **Work Orders & Scheduling**, select **Work Order**s.

3.  Click the **New** button.

4.  Configure the New Work Order as follows:

    -   **Service Account:** *A. Datum Corporation*

    -   **Incident Type:** *Service Printer*

    -   **Taxable:** *No*

5.  Click the **Save and Close** button

6.  Wait about 30 seconds to a minute and open the work order you just created.

7.  Select the **Products** tab and verify that the **Remote Printer Product**
    was added.

8.  Select the **Services** tab and verify that the **Printer Service Fee** was
    added.

9.  Select the **Service Tasks** tab and verify that the three tasks we added.

10. Click the **Related** tab and select **Characteristics**.

11. Verify that the two Characteristics defined on the Incident Type we added.
