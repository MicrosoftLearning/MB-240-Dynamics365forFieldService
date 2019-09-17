Practice Lab 3 - Resource Configuration
====================

##Scenario

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

Exercise 2 – Resource Configuration 
====================================

## Task 1 – Add yourself as a contact record in Dynamics 365
----------------------------------------------------------

1.  Using the **Sitemap**, select **Field Service.**

2.  Expand the Sitemap and Select **Contacts**.

3.  Click **New** button to create a new **Contact Record**.

4.  Configure the new **Contact** record as follows:

    -   **First Name:** *Your First Name*

    -   **Last Name:** *Your Last Name*

    -   **Job Title:** *Installer*

    -   **Email:** *Your Email Address*

    -   **Mobile Phone:** *Your Mobile Number*

    -   **Address 1 Street 1:** *Your Street Address*

    -   **Address 1 City:** *Your City*

    -   **Address 1 State Province:** *Your State*

    -   **Address 1 Zip/Postal Code:** *Your Postal Code*

Task 2 - Create a Bookable Resource for your user record
---------------------------------------------------------

1.  Using the **Sitemap**, select **Resources** under **Schedule Settings.**

2.  Click **New** button to create a new **Bookable Resource**.

3.  Configure the new **Bookable Resource** record as follows:

    -   **Resource Type:** *Contact*

    -   **User:** *The Contact Record you created in the last task*

    -   **Time Zone:** Leave the default value in the Time Zone Field.

4.  Select the **Scheduling** tab.

5.  Set the **Organizational Unit** field to **Seattle.**

6.  In the **Start Location** field, select **Organizational Unit Address**.

7.  In the **End Location** field, select **Organizational Unit Address**.

8.  Select the **Field Service** tab

9.  Set the **Hourly Rate** field to **175**.

10. **Save** the bookable resource record and leave it open.

11. Locate the **Characteristics** sub-grid, click **Add New Bookable Resource
    Characteristic**

12. Configure as follows:

    -   **Characteristic:** *Building Security*

    -   **Rating Value**: *Level 5 Security*

    -   Click **Save and Close** on the characteristic record.

13. Select **Add New Bookable Resource Characteristic** Again

14. Configure as follows:

    - **Characteristic:** *CISM*

    - **Rating Value**: *Proficient*

    - Click **Save and Close** on the characteristic record.

15. Select **Add New Bookable Resource Characteristic** Again

16. Configure as follows:

    - **Characteristic:** *CISSP*

    - **Rating Value**: *Familiar*

    - Click **Save and Close** on the characteristic record.

17. Select **Add New Bookable Resource Category Assn**

18. Configure as follows:

    -  **Resource Category:** *Installation Specialist*

    -  Click **Save and Close** on the Category record.

19. Select **Add New Bookable Resource Category Assn** again.

20. Configure as follows:

    - **Resource Category:** *Security Analyst*

    - Click **Save and Close** on the Category record.

21. **Save and Close** the bookable resource record**.**

22. Select the **Related** tab.

23. From the menu that appears, select **Resource Territory**.

24. Click the **Add New Resource Territory** button.

25. In the **Territory Lookup** field, select **WA**.

26. Select the **Save and Close** button.

27. Select the **Show Work Hours** button.

28. In the Calendar view, click the **Set Up** drop-down button.

29. From the menu that appears, choose **New Weekly Schedule**.

30. Leave the working hours as **Are the same for each day** and click the **Set
    Work Hours** Hyperlink.

31. Ensure the Work Hour are set to **8:00 AM** to **5:00 PM** and click **OK**

32. Uncheck **Sun** and **Sat**.

33. Click **Save and Close**.

34. Verify that the schedule is showing 8:00 AM to 5:00 PM – Monday – Friday
    from today forward.

35. Close the Work Hours Calendar.
