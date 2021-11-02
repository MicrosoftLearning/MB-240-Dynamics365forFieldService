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

Exercise 1 – Map Configuration 
======================================================  

## Task 1 - Enable Bing Maps to use with Resource Scheduling 

To ensure that you are able to take full advantage of the full scheduling and
mapping capabilities available with Field Service, you need to ensure that it is
configured to use a mapping provider.  Bings Maps is the default map provider,
but additional providers could be enabled.  We will be using Bing Maps. 

1.  In **Dynamics 365**, click the **Field Service** text in the navigation bar, and
    select **Resource Scheduling**.   

2.  Click the **Site Map** icon in the bottom left corner which will currently show **Resource Scheduling** to
    expand. Click on **Settings.**  From the menu that
    appears, select **Administration**.   

3.  Select **Scheduling Parameters**. 

4.  Locate the **Connect to Maps** field and set it to **Yes**. (Select OK from the popup)

5.  **Save and Close** the settings.   

Exercise 2 - Configure Dynamics 365 for Field Service
=====================================================

In this exercise, you will be modifying and configuring several Field
Service settings that will be used throughout the application. This will
include defining Skills & Certifications, Territories, Resources, and more.

Task 1 - Define Territories
---------------------------

1.  Switch applications from **Resource Scheduling** to **Field Service.** Click the **Site Map** icon in the bottom left corner to expand.  Click on **Settings.**

2.  In the left column, click **Territories.**

3.  Click **+New**.

4.  Enter **[your prefix ex. mollyc]+ North** for **Name** and click **Save**. After saving, click **+New**

5.  Enter **[your prefix ex. mollyc]+ South** for **Name** and click **Save.** After saving, click
    **+New**.

6.  Create two more Territories and name them **[your prefix ex. mollyc]+ East** and **[your prefix ex. mollyc]+ West**.

7.  You will now have four additional Territories.

Exercise 3 - Create Service Based product, and Add to Price List 
=================================================================

Task 1 - Add Printer Products
----------------------------

1.  Using the **Sitemap**, select **Products** under **General.**

2.  Click the **Add Product** to create a Product

3.  Define the Details of the Product as noted below:

-   **Name:** *[your prefix ex. mollyc]+ Remote Printer*

-   **Product ID:** *[your prefix ex. mollyc]+ Print-Serv-1234*

-   **Unit Group:** *Default Unit*

-   **Default Unit:** *Primary Unit*

-   **Decimals Supported:** *2*

4.  Select the **Field Service** tab, set the Field Service Product Type to
    **Inventory**

5.  Set the **Taxable** field to **No**

6.  Save the product,(you may see an error that a price list was not set. You can ignore this) and click **Publish** (Click **Confirm** on the popup)

7.  Click **Save & Close**

-----------------------------------------------------------

1.  Click the **Add Product** to create a Product

2.  Define the Details of the Product as noted below:

-   **Name:** *[your prefix ex. mollyc]+ Monthly Printer Maintenance*

-   **Product ID:** *[your prefix ex. mollyc]+ Print-Maint4*

-   **Unit Group:** *Default Unit*

-   **Default Unit:** *Primary Unit*

-   **Decimals Supported:** *2*

3.  Select the **Field Service** tab, set the Field Service Product Type to
    **Non-Inventory**

4.  Set the **Taxable** field to **No**

5.  Save the product. (you may see an error that a price list was not set. You can ignore this.) Click **Publish** (Click **Confirm** on the popup)

6.  Click **Save & Close**

-----------------------------------------------------------

1.  Click the **Add Product** to create a Product

2.  Define the Details of the Product as noted below:

-   **Name:** *[your prefix ex. mollyc]+ Printer Service Fee*

-   **Product ID:** *[your prefix ex. mollyc]+ Printer-Service-Fee*

-   **Unit Group:** *Default Unit*

-   **Default Unit:** *Primary Unit*

-   **Decimals Supported:** *2*

3.  Select the **Field Service** tab, set the Field Service Product Type to
    **Service**

4.  Set the **Taxable** field to **No**

5.  Save the product. (you may see an error that a price list was not set. You can ignore this.) Click **Publish** (Click **Confirm** on the popup)

Task 2 - Add Printer Products to a Price List
---------------------------------------------

1.  Using the **Sitemap**, select **Price Lists** under **Settings.**

2.  Open the **Default Price List** (Note: Change the view to **All Price Lists** if it is not already showing)

3.  Click **Activate** to activate the **Default Price List** if it is not already active.

4.  In the **Price List Items** tab, click the **+ New Price List Item** button to add a Price List
    Line Item

5.  Enter the following information:

    1.  **Product:** *[your prefix ex. mollyc]+ Remote Printer*

    2.  **Unit:** Primary Unit
    
    3.  Click the **Pricing Information** tab

    4.  **Pricing Method:** Currency Amount

    5.  **Amount:** $1000.00
    
    6.  Click **Save & Close**
    
-----------------------------------------------------------

1.  In the **Price List Items**, click the **+ New Price List Item** button to add a Price List
    Line Item

2.  Enter the following information:

    1.  **Product:** *[your prefix ex. mollyc]+ Monthly Printer Maintenance*

    2.  **Unit:** Primary Unit
    
    3.  Click the **Pricing Information** tab

    4.  **Pricing Method:** Currency Amount

    5.  **Amount:** $750.00
    
    6.  Click **Save and Close**
    
-----------------------------------------------------------

1.  In the **Price List Items**, click the **+ New Price List Item** button to add a Price List
    Line Item

2. Enter the following information:

    1.  **Product:** *[your prefix ex. mollyc]+ Printer Service Fee*

    2.  **Unit:** Primary Unit
    
    3. Click the **Pricing Information** tab

    4.  **Pricing Method:** Currency Amount

    5.  **Amount:** $150.00
    
    6. Click **Save and Close**

3. Close the Default Price List by clicking **Save & Close**

