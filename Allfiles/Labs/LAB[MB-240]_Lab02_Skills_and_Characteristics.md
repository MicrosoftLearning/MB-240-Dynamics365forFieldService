Practice Lab 2 - Skills and Characteristics 
====================

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
====================

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

Exercise 2 - Configure Dynamics 365 for Field Service Skills and Characteristics
================================================================================

Each technician that goes out to service customers may have a number of
different skills and roles assigned to them. There are three primary roles
that tech may have:

-   Installation Specialist

-   Site Inspector

-   Security Analyst

Additionally, each technician may have specific skills or Certifications
that relate to a specific product or service. The most common certifications
might be any of the following:

-   **CISM:** Certified Information Security Manager.

-   **CISSP:** Certified Information Systems Security Professional.

-   **G SEC:** GIAN Security Essentials

Since some of your customers are government agencies, technicians may need
to have specific security clearance levels. These can range from Level one
to Level five.

## Task 1 – Create a Security clearance Proficiency Model

In this task you will create a proficiency model that contains the five
different security clearance levels that can be applied.

1.  In your Dynamics 365 organization, select the down arrow next to the
    **Dynamics 365** text, select **Field Service**.

2.  Using the sitemap, select the **ellipsis**, and choose **Resource
    Scheduling**

3.  Under **Schedule Settings**, select **Proficiency Models.**

4.  From the Command Bar, select the **New** button.

5.  In the **Name** field enter **Security Level**.

6.  Set the **Min Rating Value** to **1**.

7.  Set the **Max Rating Value** to 5.

8.  Click the **Save** button to save the record and leave it open.

9.  Select the **Related** tab and choose **Rating Values** from the menu that
    appears.

10. In the **Rating Values** tab, select the **Add New Rating Value** button.

11. In the **Name** field, enter **Level 1 Security**.

12. Set the **Value** field to **1**.

13. Ensure the **Rating Model** is set to **Security Level** and click the
    **Save and Close** button.

14. Select the **Add New Rating Value** button.

15. In the **Name** field, enter **Level 2 Security**.

16. Set the **Value** field to **2**.

17. Ensure the **Rating Model** is set to **Security Level** and click the
    **Save and Close** button.

18. Select the **Add New Rating Value** button.

19. In the **Name** field, enter **Level 3 Security**.

20. Set the **Value** field to **3**.

21. Ensure the **Rating Model** is set to **Security Level** and click the
    **Save and Close** button.

22. Select the **Add New Rating Value** button.

23. In the **Name** field, enter **Level 4 Security**.

24. Set the **Value** field to **4**.

25. Ensure the **Rating Model** is set to **Security Level** and click the
    **Save and Close** button.

26. Select the **Add New Rating Value** button.

27. In the **Name** field, enter **Level 5 Security**.

28. Set the **Value** field to **5**.

29. Ensure the **Rating Model** is set to **Security Level** and click the
    **Save and Close** button.

30. Verify that the Security Level Model has 5 Security levels added to it.

## Task 2 - Define your Security Clearance Skill

In this task you will create a building security skill that will be used in
conjunction with the Proficiency Model you defined in the previous task.

1.  In your Dynamics 365 organization, select the down arrow next to the
    **Dynamics 365** text, select **Field Service**.

2.  Using the sitemap, select the **ellipsis**, and choose **Field Service
    Settings**

3.  Under **Schedule Settings**, select **Characteristics**.

4.  Select the **New** button.

5.  In the **Name** field, enter **Building Security**

6.  Set the **Certification Type** field to **Skill** and click the **Save**
    button.

## Task 3 - Define your required Certification Characteristics

In this task you will be adding the **CISM:** Certified Information Security
Manager, **CISSP:** Certified Information Systems Security Professional, and **G
SEC:** GIAN Security Essentials certifications and resource skills.

1.  In your Dynamics 365 organization, select the down arrow next to the
    **Dynamics 365** text, select **Field Service**.

2.  Using the sitemap, select the **ellipsis**, and choose **Field Service
    Settings**

3.  Under **Schedule Settings**, select **Characteristics**.

4.  Select the **New** button.

5.  In the **Name** field, enter **CISM**

6.  Set the **Certification Type** field to **Certification** and click the
    **Save** button.

7.  Select the **New** button again.

8.  In the **Name** field, enter **CISSP**

9.  Set the **Certification Type** field to **Certification** and click the
    **Save** button.

10. Select the **New** button one last time.

11. In the **Name** field, enter **G SEC**

12. Set the **Certification Type** field to **Certification** and click the
    **Save** button.

13. Verify that **CISM**, **CISSP**, and **G SEC** have all been added as
    Characteristics.

## Task 4 - Define Resource Categories

In this task, you will be adding the Installation Specialist, Site Inspector,
and Security Analyst resource roles.

1.  Using the **Sitemap**, select **Resource Categories** under **Schedule
    Settings.**

2.  Click **New**.

3.  In the **Name** field, enter **Installation Specialist.**

4.  Enter **Installation Specialist** in the **Description** field as well and
    click the **Save** button.

5.  Click **New** button again.

6.  In the **Name** field, enter **Site Inspector.**

7.  Enter **Site Inspector** in the **Description** field as well and click the
    **Save** button.

8.  Click **New** button one last time.

9.  In the **Name** field, enter **Security Analyst.**

10. Enter **Security Analyst** in the **Description** field as well and click
    the **Save** button.

11. Verify that the Security Analyst, Installation Specialist, and Site
    Inspector roles have been added.
