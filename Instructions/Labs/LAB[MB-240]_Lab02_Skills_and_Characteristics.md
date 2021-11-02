---
lab:
    title: 'Lab: Skills and characteristics'
    module: 'Module 2: Resource Scheduling Configuration'
---

Module 2 - Resource Scheduling Configuration
====================
## Practice Lab 2 - Skills and characteristics 

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

Exercise 1 - Configure Dynamics 365 for Field Service Skills and Characteristics
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
    **Dynamics 365** text, select **Resource Scheduling**.

2.  Using the sitemap, select the **Settings**

3.  Under **Resource**, select **Proficiency Models.**

4.  From the Command Bar, select the **+New** button.

5.  In the **Name** field enter **[your prefix ex. mollyc]+ Security Level**.

6.  Set the **Min Rating Value** to **1**.

7.  Set the **Max Rating Value** to 5.

8.  Click the **Save** button to save the record and leave it open.

9.  Click the **Related** tab, and select **Rating Values**

10. In the **Rating Values** section, select **+ New Rating Value** button.

11. In the **Name** field, enter **[your prefix ex. mollyc]+ Level 1 Security**.

12. Set the **Value** field to **1**.

13. Ensure the **Rating Model** is set to **[your prefix ex. mollyc]+ Security Level** and click the
    **Save and Close** button.

14. Select the **+ New Rating Value** button.

15. In the **Name** field, enter **[your prefix ex. mollyc]+ Level 2 Security**.

16. Set the **Value** field to **2**.

17. Ensure the **Rating Model** is set to **[your prefix ex. mollyc]+ Security Level** and click the
    **Save and Close** button.

18. Select the **Add New Rating Value** button.

19. In the **Name** field, enter **[your prefix ex. mollyc]+ Level 3 Security**.

20. Set the **Value** field to **3**.

21. Ensure the **Rating Model** is set to **[your prefix ex. mollyc]+ Security Level** and click the
    **Save and Close** button.

22. Select the **Add New Rating Value** button.

23. In the **Name** field, enter **[your prefix ex. mollyc]+ Level 4 Security**.

24. Set the **Value** field to **4**.

25. Ensure the **Rating Model** is set to **[your prefix ex. mollyc]+ Security Level** and click the
    **Save and Close** button.

26. Select the **Add New Rating Value** button.

27. In the **Name** field, enter **[your prefix ex. mollyc]+ Level 5 Security**.

28. Set the **Value** field to **5**.

29. Ensure the **Rating Model** is set to **[your prefix ex. mollyc]+ Security Level** and click the
    **Save and Close** button.

30. Verify that the Security Level Model has 5 Security levels added to it.

## Task 2 - Define your Security Clearance Skill

In this task you will create a building security skill that will be used in
conjunction with the Proficiency Model you defined in the previous task.

1.  In your Dynamics 365 organization, select the down arrow next to the
    **Dynamics 365** text, select **Resource Scheduling**.

2.  Using the sitemap, select **Settings**

3.  Under **Resource**, select **Skills**.

4.  Select the **+New** button.

5.  In the **Name** field, enter **[your prefix ex. mollyc]+ Building Security**

6.  Set the **Characteristic Type** field to **Skill** and click the **Save**
    button.

## Task 3 - Define your required Certification Characteristics

In this task you will be adding the **CISM:** Certified Information Security
Manager, **CISSP:** Certified Information Systems Security Professional, and **G
SEC:** GIAN Security Essentials certifications and resource skills.

1.  In your Dynamics 365 organization, select the down arrow next to the
    **Dynamics 365** text, select **Resource Scheduling**.

2.  Using the sitemap, select **Settings**

3.  Under **Resource**, select **Skills**.

4.  Select the **+New** button.

5.  In the **Name** field, enter **[your prefix ex. mollyc]+ CISM**

6.  Set the **Characteristic Type** field to **Certification** and click the
    **Save** button.

7.  Select the **+New** button again.

8.  In the **Name** field, enter **[your prefix ex. mollyc]+ CISSP**

9.  Set the **Characteristic Type** field to **Certification** and click the
    **Save** button.

10. Select the **New** button one last time.

11. In the **Name** field, enter **[your prefix ex. mollyc]+ G SEC**

12. Set the **Characteristic Type** field to **Certification** and click the
    **Save** button.

13. Verify that **[your prefix ex. mollyc]+ CISM**, **[your prefix ex. mollyc]+ CISSP**, and **[your prefix ex. mollyc]+ G SEC** have all been added as
    Skills.

## Task 4 - Define Resource Categories

In this task, you will be adding the Installation Specialist, Site Inspector,
and Security Analyst resource roles.

1.  In your Dynamics 365 organization, select the down arrow next to the
    **Dynamics 365** text, select **Resource Scheduling**.

2.  Using the sitemap, select **Settings**

3.  Under **Resource**, select **Roles**.

4.  Select **+New**

5.  In the **Name** field, enter **[your prefix ex. mollyc]+ Installation Specialist.**

6.  Enter **[your prefix ex. mollyc]+ Installation Specialist** in the **Description** field as well and
    click the **Save** button.

7.  Click **+New** button again.

8.  In the **Name** field, enter **[your prefix ex. mollyc]+ Site Inspector.**

9.  Enter **[your prefix ex. mollyc]+ Site Inspector** in the **Description** field as well and click the
    **Save** button.

10.  Click **New** button one last time.

11.  In the **Name** field, enter **[your prefix ex. mollyc]+ Security Analyst.**

12. Enter **[your prefix ex. mollyc]+ Security Analyst** in the **Description** field as well and click
    the **Save** button.

13. Verify that the [your prefix ex. mollyc]+ Security Analyst, [your prefix ex. mollyc]+ Installation Specialist, and [your prefix ex. mollyc]+ Site
    Inspector roles have been added.
