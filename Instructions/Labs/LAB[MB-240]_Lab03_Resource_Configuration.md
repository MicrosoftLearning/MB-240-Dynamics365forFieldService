---
lab:
    title: 'Lab: Resource configuration'
    module: 'Module 3: Defining and Configuring Bookable Resources'
---

Module 3 - Defining and Configuring Bookable Resources
====================
## Practice Lab 3 - Resource configuration

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

Select the **Field Service** app from the list.

Exercise 2 – Resource Configuration 
====================================

Task 1 - Create a Bookable Resource for your user record
---------------------------------------------------------

1.  Using the **Sitemap**, select **Resources**

2.  Click **New** button to create a new **Bookable Resource**.

3.  Configure the new **Bookable Resource** record as follows:

    -   **Resource Type:** *User*

    -   **User:** *The Contact record you are signed in as (example **alans or Alan Steiner**)*

    -   **Time Zone:** Leave the default value in the Time Zone Field.

4.  Select the **Scheduling** tab.

5.  Set the **Organizational Unit** field to **Seattle.**

6.  In the **Start Location** field, select **Organizational Unit Address**.

7.  In the **End Location** field, select **Organizational Unit Address**.

8.  Select the **Field Service** tab

9.  Set the **Hourly Rate** field to **175**.

10. **Save** the bookable resource record and leave it open.

11. Locate the **Characteristics** sub-grid, ensure the view is **Active Bookable Resource Characteristics** and select **+New** (note: change the form view to **Information** by clicking the dropdown arrow.)

12. Configure as follows:

    - **Characteristic:** *Building Security*

    - **Rating Value**: *Level 5 Security*
    
    - **Resource**: *your user*

    - Click **Save and Close** on the characteristic record.

13. Select **+New** Again

14. Configure as follows:

    - **Characteristic:** *CISM*

    - **Rating Value**: *Proficient*
    
    - **Resource**: *your user*

    - Click **Save and Close** on the characteristic record.

15. Select **+New** Again

16. Configure as follows:

    - **Characteristic:** *CISSP*

    - **Rating Value**: *Familiar*
    
    - **Resource**: *your user*

    - Click **Save and Close** on the characteristic record.

Select **Resources** from the sitemap

1. Select *your user*

2. Select the **Related** tab and select **Resource Category Assns**

3. Select **+New Bookable Resource Category Assn**

4. Configure as follows:

    -  **Name:** *Installation Specialist*
    
    -  **Resource Category** *Installation Specialist*

    -  Click **Save and Close** on the Category record.

5. Select **+New Bookable Resource Category Assn** again.

6. Configure as follows:

    - **Name** *Security Analyst*
    
    - **Resource Category:** *Security Analyst*

    - Click **Save and Close** on the Category record.

7. **Save and Close** the bookable resource record**.**

8. Select *your user*

9. Select the **Related** tab.

10. From the menu that appears, select **Resource Territories**.

11. Click the **+New Resource Territory** button.

12. In the **Territory Lookup** field, select **WA**.

13. Select the **Save and Close** button.

14. Select the **Work Hours** tab. (Note: click the **Related** tab if you don't see it)

15. In the Calendar view, click **+New** dropdown arrow and select **Working hours**.

16. From the menu that appears, choose **Every Week** from the repeat field.

17. Ensure the Work Hour are set to **8:00 AM** to **5:00 PM**

18. Ensure **Sun** and **Sat** are unchecked, and **Mo** thru **Fr** are checked.

19. Click **Save**.

20. Verify that the schedule is showing 8:00 AM to 5:00 PM – Monday – Friday
    from today forward.

21. Click **Save & Close**.
