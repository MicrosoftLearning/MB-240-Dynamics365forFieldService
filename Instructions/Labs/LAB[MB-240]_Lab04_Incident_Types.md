---
lab:
    title: 'Lab: Incident types'
    module: 'Module 4: Configure Incidents'
---

Module 4 - Configure Incidents
====================
## Practice Lab 4 - Incident types

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

1.  Sign into the Virtual Machine using the lab instructions provided by the lab hoster (if using).

2.  Outside the VM in the online lab interface click Files and choose D365
    Credentials. This will allocate a Dynamics 365 365 tenant for you to use in these
    labs.  It will display the user email and password for your tenant. 

3.  Launch Microsoft Edge from the taskbar. 

4.  Navigate in the browser to the Power Platform admin portal at https://admin.Powerplatform.microsoft.com.

5. Sign in using the provided credentials. Record the characters before the "@" symbol in your email address - it should be a first name and a last initial. These characters will become your "alias" throughout the course. Write them down somewhere you'll be able to access throughout the course.

**Important:** Please be aware that this tenant and the Dynamics 365 organization will be shared with the other students in your classroom, like employees would share a tenant when using the Dynamics 365 instance belonging to their organization. Do not use any PII (personally identifiable information) when creating records. It is also good practice to use your username prefix (ex., **mollyc**) in front of all records, data, apps, workflows, etc. you create.

6. Click the button to the left of the **Power Platform admin center** in the top menu to view all available apps. Select **Dynamics 365.**

7. Select the Field Service app from the list.


Exercise 2 – Create an Incident Type called Printer Installation
================================================================

### Task 1 –Service Task Types to be used with Incidents:

1.  Using the **Sitemap**, select **Settings

2.  Select  **Service Task Types** under **Work Order** settings

3.  Click the **+New** button and enter **[your prefix ex. mollyc]+ Clean Printer Assembly** for the Name.

4.  Select **30 Minutes** for the **Estimated Duration.**

5.  Click **Save and Close.**

6.  Repeat Steps 2 – 4 to add each of the following:

    1.  **[your prefix ex. mollyc]+ Replace Toner:** *Duration 15 Minutes*

    2.  **[your prefix ex. mollyc]+ Finial Test:** *Duration 15 Minutes*
    
### Task 2 - Create a Service Call Work Order Type

1. Using the **Sitemap**, select **Work Order Types**

2. Click the **+New** button and enter **[your prefix ex. mollyc]+ Service Call** for the Name.

3. Set **Incident Required** and **Taxable** to **No**

4. Click **Save & Close**

### Task 3 –Create a Service Printer Incident Type

1.  Using the **Sitemap**, select **Incident Types** under **Work Order**
    settings.

2.  Click the **New** button and enter **[your prefix ex. mollyc]+ Service Printer** for the Name.

3.  Select the Details tab, and configure as follows:

-   **Copy Incident Items to Agreement:** *Yes*

-   Click **Default Work Order Type** and select  *[your prefix ex. mollyc]+ Service Call*.

1.  Click **Save** to save the Incident type and leave it open.

2.  Select the **Service Task** Tab, click the ellipsis and select **+New Incident Type Service Tasks** button. (If pop ups are blocked, you may need to unblock them)

3.  Enter **[your prefix ex. mollyc]+ Clean Printer Assembly** for the **Name**, select **[your prefix ex. mollyc]+ Clean Printer
    Assembly** as the task type, ensure 30 minutes is set for **Estimated
    Duration**.

4.  Click **Save and Close.**

5.  Click the **+New Incident Type Service Tasks** button again.

6.  Enter **[your prefix ex. mollyc]+ Replace Toner** for the **Name**, select **[your prefix ex. mollyc]+ Replace Toner** as the
    task type, ensure 15 minutes is set for **Estimated Duration**.

7.  Click **Save and Close.**

8.  Click the **Add Incident Type Service Tasks** button one last time.

9.  Enter **[your prefix ex. mollyc]+ Finial Test** for the **Name**, select **[your prefix ex. mollyc]+ Finial Test** as the task
    type, ensure 15 minutes is set for **Estimated Duration**.

10. Click **Save and Close.**

11. Select the **Products** tab

12. Click the ellipsis and select **+ New Incident Type Product** button.

13. Configure the Incident Type Product as follows:

    -   **Name:** *[your prefix ex. mollyc]+ Remote Printer*

    -   **Unit:** *Primary Unit*

    -   **Quantity:** *1*

    -   **Product:** *[your prefix ex. mollyc]+ Remote Printer*

14. Click the **Save and Close** button

15. Select the **Services** Tab.

16. Click the ellipsis and select **+New Incident Type Service** button.

17. Configure the new Incident Type Service as follows:

    -   **Name:** *[your prefix ex. mollyc]+ Printer Service Fee*

    -   **Unit:** *Primary Unit*

    -   **Service** *[your prefix ex. mollyc]+ Printer Service Fee*

18. Click the **Save and Close** Button

19. Select the **Characteristics** tab

20. Click the ellipsis and select **+New Incident Type Characteristics** button

21. Configure the Incident Type Characteristic as follows:

    -   **Characteristic:** *[your prefix ex. mollyc]+ CISM*

    -   **Rating Value:** *Familiar*

22. Click the **Save and Close** button

23. Click the **+New Incident Type Characteristics** button again

24. Configure the Incident Type Characteristic as follows:

    -   **Characteristic:** *[your prefix ex. mollyc]+ Building Security*

    -   **Rating Value:** *[your prefix ex. mollyc]+ Level 2 Security*

25. Click the Save and Close Button

Exercise 3 – Test your Configuration Settings
=============================================

### Task 1 –Create a new Work Order using Service Printer Incident Type:

1.  Using the **Sitemap**, select **Service**.

2.  Under **Work Orders**, under **Scheduling**.

3.  Click the **+New** button.

4.  Configure the New Work Order as follows:

    -   **Service Account:** *A. Datum*
    
    -   **Work Order Type** *[your prefix ex. mollyc]+ Service Call*
    
    -   **Price List** *Default Price List*
    
    -   **Taxable** *No*

    -   **Primary Incident Type:** *[your prefix ex. mollyc]+ Service Printer*

5.  Click the **Save and Close** button

6.  Wait about 30 seconds to a minute and open the work order you just created.

7.  Select the **Products** tab and verify that the **[your prefix ex. mollyc]+ Remote Printer Product**
    was added.

8.  Select the **Services** tab and verify that the **[your prefix ex. mollyc]+ Printer Service Fee** was
    added.

9.  Select the **[your prefix ex. mollyc]+ Service Tasks** tab and verify that the three tasks we added.

10. Click the **Related** tab and select **Characteristics**.

11. Verify that the two Characteristics defined on the Incident Type we added.
