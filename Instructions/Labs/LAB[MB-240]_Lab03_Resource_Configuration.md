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

Exercise 1 – Resource Configuration 
====================================

Task 1 - Create a Bookable Resource for your user record
---------------------------------------------------------

1.  In your Dynamics 365 organization, select the down arrow next to the **Dynamics 365** text, select **Field Service**.

2.  Using the **Sitemap**, select **Resources**

3.  Under **Resource**, select **Resources**

3.  Click **New** button to create a new **Bookable Resource**.

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

    - **Characteristic:** *[your prefix ex. mollyc]+ Building Security*

    - **Rating Value**: *[your prefix ex. mollyc]+ Level 5 Security*
    
    - **Resource**: *your user*

    - Click **Save and Close** on the characteristic record.

13. Select **+New** Again

14. Configure as follows:

    - **Characteristic:** *[your prefix ex. mollyc]+ CISM*

    - **Rating Value**: *Proficient*
    
    - **Resource**: *your user*

    - Click **Save and Close** on the characteristic record.

15. Select **+New** Again

16. Configure as follows:

    - **Characteristic:** *[your prefix ex. mollyc]+ CISSP*

    - **Rating Value**: *Familiar*
    
    - **Resource**: *your user*

    - Click **Save and Close** on the characteristic record.

Select **Resources** from the sitemap

1. Select *your user*

2. Select the **Related** tab and select **Resource Category Assns**

3. Select **+New Bookable Resource Category Assn**

4. Configure as follows:

    -  **Name:** *[your prefix ex. mollyc]+ Installation Specialist*
    
    -  **Resource Category** *[your prefix ex. mollyc]+ Installation Specialist*

    -  Click **Save and Close** on the Category record.

5. Select **+New Bookable Resource Category Assn** again.

6. Configure as follows:

    - **Name** *[your prefix ex. mollyc]+ Security Analyst*
    
    - **Resource Category:** *[your prefix ex. mollyc]+ Security Analyst*

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
