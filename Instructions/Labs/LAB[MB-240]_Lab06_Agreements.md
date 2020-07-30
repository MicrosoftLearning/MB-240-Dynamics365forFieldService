---
lab:
    title: 'Lab: Agreements'
    module: 'Module 6: Field Service Agreements'
---

Module 6 - Field Service Agreements
=====================
## Practice Lab 6 - Agreements

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
=========================

### Task 1 – Connect to the Power Platform administration portal

1.  Sign into the Virtual Machine using the lab instructions provided by the lab hoster (if using).

2.  Outside the VM in the online lab interface click Files and choose D365
    Credentials. This will allocate a Dynamics 365 365 tenant for you to use in these
    labs.  It will display the user email and password for your tenant. 

3.  Launch Microsoft Edge from the taskbar. 

4.  Navigate in the browser to the Power Platform admin portal at https://admin.Powerplatform.microsoft.com.

5. Sign in using the provided credentials. Record the characters before the "@" symbol in your email address - it should be a first name and a last initial. These characters will become your "alias" throughout the course. Write them down somewhere you'll be able to access throughout the course.

**Important:** Please be aware that this tenant and the Dynamics 365 organization will be shared with the other students in your classroom, like employees would share a tenant when using the Dynamics 365 instance belonging to their organization. Do not use any PII (personally identifiable information) when creating records. It is also good practice to use your username prefix (ex., **mollyc**) in front of all records, data, apps, workflows, etc. you create.

6. Click the button to the left of the **Power Platform admin center** in the top menu to view all available apps. Select **Dynamics 365.**

Select the Field Service app from the list.

Exercise 2 - Create Field Service related products, and add to Price List 
==============================

Before you can define products associated with Agreements, they need to be added to the product catalog. In this exercise, you will be defining three new products:

-   A Remote Printer

-   Monthly Printer Maintenance

-   Printer Service Fee

## Task 1 - Add a Printer Products

Note: If you have already completed this step in a previous lab, skip to Exercise 3.

1.  Using the **Sitemap**, select **Products** under **Settings.**

2.  Click the **Add Product** to create a Product

3.  Define the Details of the Product as noted below:

	-   **Name:** Remote Printer

	-   **Product ID:** *Print-Serv-1234*

	-   **Unit Group:** *Default Unit*

	-   **Default Unit:** *Primary Unit*

	-   **Decimals Supported:** *2*

4.  Select the **Field Service** tab, set the Field Service Product Type to
    **Inventory**

	-  Set the **Taxable** field to **No**

	-  Save the product, and click **Publish**

6.  Return to the Products page. Click the **Add Product** to create a Product

7.  Define the Details of the Product as noted below:

	-   **Name:** Monthly Printer Maintenance

	-   **Product ID:** *Print-Maint4*

	-   **Unit Group:** *Default Unit*

	-   **Default Unit:** *Primary Unit*

	-   **Decimals Supported:** *2*

8.  Select the **Field Service** tab, set the Field Service Product Type to
    **Non-Inventory**

9.  Set the **Taxable** field to **No**

10.  Save the product, and click **Publish**

11.  Click the **Add Product** to create a Product

12.  Define the Details of the Product as noted below:

	-   **Name:** Printer Service Fee

	-   **Product ID:** *Print-Service-Fee*

	-   **Unit Group:** *Default Unit*

	-   **Default Unit:** *Primary Unit*

	-   **Decimals Supported:** *2*

13.  Select the **Field Service** tab, set the Field Service Product Type to
    **Service**

14.  Set the **Taxable** field to **No**

15.  Save the product, and click **Publish**

## Task 2 - Add a Printer Products to a Price List

1.  Using the **Sitemap**, select **Price Lists** under **Settings.**

2.  Open an exisitng price list.

3.  In the **Price List Items**, click the **+ Add** button to add a Price List
    Line Item

4.  Enter the following information:

    - **Product:** Remote Printer

    - **Unit:** Primary Unit

    - **Pricing Method:** Currency Amount

    - **Amount:** $1000.00

5.  In the **Price List Items**, click the **+ Add** button to add a Price List
    Line Item

6.  Enter the following information:

    - **Product:** Monthly Printer Maintenance

    - **Unit:** Primary Unit

    - **Pricing Method:** Currency Amount

    - **Amount:** \$750.00

7.  Click **Save and Close**

8.  In the **Price List Items**, click the **+ Add** button to add a Price List
    Line Item

9.  Enter the following information:

    - **Product:** Printer Service Fee

    - **Unit:** Primary Unit

    - **Pricing Method:** Currency amount

    - **Amount:** \$150.00

10. Click **Save and Close**

11. Close the price list

Exercise 3 - Create an Agreement 
================================

In this exercise you will be defining a preventative maintenance agreement that
will generate Work orders monthly and quarterly. Additionally, the customer will
be billed at the end of each month with a Monthly Printer Maintenance fee.

## Task 1 - Create an Agreement to be used for Preventative Maintenance 

1.  In Dynamics 365, navigate to **Field Service**

2.  Using the Sitemap, select **Agreements** under the **Service Delivery**
    heading.

3.  Click **New** from the Command Bar.

4.  Select **Coho Winery** for the **Service Account**.

5.  Under Details set the fields as follows:

    - **Start Date:** Today’s Date

    - **End Date:** 1 Year from Today

6.  Set the **Price List** to **Default Price List** and **Taxable** to **No**.

7.  Click the **Save** to save the agreement and leave it open.

## Task 2 - Setup an Automated Booking for the Agreement

1.  In the agreement that you just created, click on the **New Agreement Booking Setup** button in the
    Booking Setups area.

2.  Configure the Agreement Booking as follows:

    - **Name:** Coho Monthly Printer Service

    - **Auto Generate Work Order**: Yes

    - **Work Order Type:** Preventative Maintenance

    - **Auto Generate Booking**: No

    - **Estimated Duration:** 1 Hour

    - **Pre Booking Flexibility:** 1

    - **Post Booking Flexibility:** 1

    - **Time Window Start:** 9:00 AM

    - **Time Window End:** 12:00 PM

    - **Generate Work Order Days in Advance**: 2 (to ensure that the work
        order is created right away, determine how many days are left in the
        current month, and use that number or greater for this value)

3.  Save the record and leave it open.

4.  Under **Incidents,** click **New Agreement Booking Incident.**

5.  Select **Install IOT** for Incident Type and click **Save & Close.**

6.  On the Agreement Booking Setup Record, click the ellipsis and select **Booking Recurrence**.

7.  Set the Recurrence Patten as noted below:

    - **Monthly:** on the 1st day of every One Month

    - Start on the 1st day of Next Month

    - End After 12 Occurrences

8.  Verify the changes have saved, and close the Booking Setup Record.

9.  In the agreement that you just created, click on the **New Agreement Booking Setup** button in the
    Booking Setups area.

10. Configure the Agreement Booking as follows:

    - **Name:** Quarterly System Check

    - **Auto Generate Work Order**: Yes

    - **Work Order Type:** Preventative Maintenance

    - **Generate Work Order Days In Advance:** 5

    - **Priority:** Moderate

    - **Auto Generate Booking**: No

    - **Estimated Duration:** 30 Minutes

    - **Pre Booking Flexibility:** 2

    - **Post Booking Flexibility:** 4

11. Save the record and leave it open.

12. On the Agreement Booking Setup Record, click ellipsis and select **Booking Recurrence**.

13. Set the Recurrence Patten as noted below:

    - **Monthly:** on the 1st day of Every 3 Month

    - Start on the 1st day of Next Month

   - End After 12 Occurrences

14. Verify the changes have saved and close the Booking Setup Record.

15. Locate **the Invoice Setups** Sub-grid, and click the **New Agreement Invoice Setup** button to
    create a new Invoice setup

16. Enter Coho Monthly Invoice for the Name, and Click Save

17. If Necessary, expand Invoice Products, click the ellipsis and select **New Agreement Invoice Product** button to add
    Invoice Products

18. Complete the Agreement Invoice Product as follows:

    - **Product:** Monthly Printer Maintenance

    - **Unit:** Primary Unit

    - **Quantity:** 1

    - Click **Save and Close**

19. Close the Coho Monthly Invoice record

20. Return to the Agreement. Change the Agreement System Status from Estimate to
    **Active** and **Save**.
