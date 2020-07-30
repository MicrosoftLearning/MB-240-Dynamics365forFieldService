---
lab:
    title: 'Lab: Configure Dynamics 365 Field Service'
    module: 'Module 1: Configure Field Service'
---

Practice Lab 1 - Configure Dynamics 365 Field Service
=====

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
ahead to **Exercise 4.**

Exercise 1 - Acquire Tenant Information and Connect
====

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

5.  When viewing tiles of all available applications, click on “Field Service”
    to open your Dynamics 365 instance to the Field Service application. You
    have now entered your Dynamics 365 production environment and are ready to
    explore the Field Service app.

Exercise 2 – Map Configuration 
======================================================  

## Task 1 - Enable Bing Maps to use with Resource Scheduling 

To ensure that you are able to take full advantage of the full scheduling and
mapping capabilities available with Field Service, you need to ensure that it is
configured to use a mapping provider.  Bings Maps is the default map provider,
but additional providers could be enabled.  We will be using Bing Maps. 

1.  In **Dynamics 365**, click the arrow next to the **Dynamics 365** text, and
    select **Resource Scheduling**.   

2.  Click the **Site Map** icon in the bottom left corner to
    expand. Click on **Settings.**  From the menu that
    appears, select **Administration**.   

3.  Select **Scheduling Parameters**. 

4.  Locate the **Connect to Maps** field and set it to **Yes**. (Select OK from the popup)

5.  **Save and Close** the settings.   

Exercise 4 - Configure Dynamics 365 for Field Service
=====================================================

In this exercise, you will be modifying and configuring several Field
Service settings that will be used throughout the application. This will
include defining Skills & Certifications, Territories, Resources, and more.

Task 1 - Define Territories
---------------------------

1.  Switch applications from Resource Scheduling to **Field Service.** Click the **Site Map** icon in the bottom left corner to expand.  Click on **Settings.**

2.  In the left column, click **Territories.**

3.  Click **New**.

4.  Enter **[your prefix ex. mollyc]+ North** for **Name** and click **Save**. After saving, click **New**

5.  Enter **[your prefix ex. mollyc]+ South** for **Name** and click **Save.** After saving, click
    **New**.

6.  Create two more Territories and name them **[your prefix ex. mollyc]+ East** and **[your prefix ex. mollyc]+ West**.

7.  You will now have four additional Territories.

Exercise 5 - Create Service Based product, and Add to Price List 
=================================================================

Task 1 - Add Printer Products
----------------------------

1.  Using the **Sitemap**, select **Products** under **General.**

2.  Click the **Add Product** to create a Product

3.  Define the Details of the Product as noted below:

-   **Name:** [your prefix ex. mollyc]+ Remote Printer

-   **Product ID:** *[your prefix ex. mollyc]+ Print-Serv-1234*

-   **Unit Group:** *Default Unit*

-   **Default Unit:** *Primary Unit*

-   **Decimals Supported:** *2*

1.  Select the **Field Service** tab, set the Field Service Product Type to
    **Inventory**

2.  Set the **Taxable** field to **No**

3.  Save the product, and click **Publish** (Click **Confirm** on the popup)

4.  Click **Save & Close**

5.  Click the **Add Product** to create a Product

6.  Define the Details of the Product as noted below:

-   **Name:** [your prefix ex. mollyc]+ Monthly Printer Maintenance

-   **Product ID:** *[your prefix ex. mollyc]+ Print-Maint4*

-   **Unit Group:** *Default Unit*

-   **Default Unit:** *Primary Unit*

-   **Decimals Supported:** *2*

1.  Select the **Field Service** tab, set the Field Service Product Type to
    **Non-Inventory**

2.  Set the **Taxable** field to **No**

3.  Save the product, and click **Publish** (Click **Confirm** on the popup)

4.  Click **Save & Close**

5.  Click the **Add Product** to create a Product

6.  Define the Details of the Product as noted below:

-   **Name:** [your prefix ex. mollyc]+ Printer Service Fee

-   **Product ID:** *[your prefix ex. mollyc]+ Printer-Service-Fee*

-   **Unit Group:** *Default Unit*

-   **Default Unit:** *Primary Unit*

-   **Decimals Supported:** *2*

1.  Select the **Field Service** tab, set the Field Service Product Type to
    **Service**

2.  Set the **Taxable** field to **No**

3.  Save the product, and click **Publish** (Click **Confirm** on the popup)

Task 2 - Add Printer Products to a Price List
---------------------------------------------

1.  Using the **Sitemap**, select **Price Lists** under **General.**

2.  Open the **Default Price List** (Note: Change the view to **All Price Lists** if it is not already showing)

3.  Click **Activate** to activate the **Default Price List** if it is not already active.

4.  In the **Price List Items**, click the **+ New Price List Item** button to add a Price List
    Line Item

5.  Enter the following information:

    1.  **Product:** [your prefix ex. mollyc]+ Remote Printer

    2.  **Unit:** Primary Unit
    
    3.  Click the **Pricing Information** tab

    4.  **Pricing Method:** Currency Amount

    5.  **Amount:** $1000.00
    
    6.  Click **Save & Close**

6.  In the **Price List Items**, click the **+ New Price List Item** button to add a Price List
    Line Item

7.  Enter the following information:

    1.  **Product:** [your prefix ex. mollyc]+ Monthly Printer Maintenance

    2.  **Unit:** Primary Unit
    
    3.  Click the **Pricing Information** tab

    4.  **Pricing Method:** Currency Amount

    5.  **Amount:** $750.00
    
    6.  Click **Save and Close**

9.  In the **Price List Items**, click the **+ New Price List Item** button to add a Price List
    Line Item

10. Enter the following information:

    1.  **Product:** [your prefix ex. mollyc]+ Printer Service Fee

    2.  **Unit:** Primary Unit
    
    3. Click the **Pricing Information** tab

    4.  **Pricing Method:** Currency Amount

    5.  **Amount:** $150.00
    
    6. Click **Save and Close**

12. Close the Default Price List by clicking **Save & Close**

