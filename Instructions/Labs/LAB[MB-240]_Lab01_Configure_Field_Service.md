---
lab:
    title: 'Lab: Configure Dynamics 365 Field Service'
    module: 'Module 1: Configure Field Service'
---

## Important notice re: tenants - temporary workaround

As of January 23, 2020, WWL is unable to provide students with pre-provisioned Dynamics 365 access, and is working on a solution that should be available in the next 4-6 weeks. As a workaround, we are recommending using Dynamics 365 Trial accounts. Each student will be responsible for requesting these. To help students in getting the Dynamics 365 tenants (including Marketing), M365 tenants will be provided through the Authorized Lab Hosters. This is a short-term solution and we will keep all stakeholders including Learning Partners and MCTs updated as progress is made and advise as a more permanent solution timeline for pre-provisioning Dynamics 365 access for lab use is established. Please work with your Authorized Lab Hoster for provisioning of the M365 Tenants for the students and follow the instructions below to use the M365 tenant to secure a Dynamics 365 trial for your appropriate application.
 
1. Using your provided M365 credentials, log into https://admin.microsoft.com/ and accept the terms.
2. Once you’ve logged in successfully, access https://trials.dynamics.com/. Select the applicable application for your course.
3. Under “Work email,” enter the email address from the M365 credentials. Under “phone number,” enter your own phone number.
4. Select Get Started.
5. You will be prompted to enter your password for the on.microsoft.com account. Enter the password provided for the M365 tenant.
6. If you are prompted to accept terms and conditions, accept them. Your environment may take a few minutes to provision.

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

5.  If prompted to select a trial, select the far-right option to install all
    applications.

    1.  **Note:** If you have already selected your trial in a previous lab
        exercise, you will be taken to the D365 Administration Center. If so,
        select the **Open** circled arrow button beside “Contoso Production.”

6.  When viewing tiles of all available applications, click on “Field Service”
    to open your Dynamics 365 instance to the Field Service application. You
    have now entered your Dynamics 365 production environment and are ready to
    explore the Field Service app.


Exercise 2 – Install Field Service Demo Data
=====

## Task 1 - Install demo data
The labs and exercises provided work best when you have sample data to work
with. Depending on if the environment you are working with, you may want to
install some sample data to assist with exercises. Dynamics 365 provides the
ability to add sample data as needed. If the environment you are working in does
not have any sample data installed, follow the steps below to install the sample
data into your environment.
   
**IMPORTANT:** *The demo data that we will be leveraging for this exercise
is a smaller set of data that will help to illustrate the configuration
concepts available in the application. There is more complete demo data
available that can be used for both Project Service automation and Field
Service.

If your demo data is in a .zip file, please follow the instructions in 1-4.
If your demo data is already in a folder on your desktop, skip to step 5.

1.  Locate the **FS_Demo_Data.zip** file available in the class resources.

2.  Right click the **FS_Demo_Data.zip** file, and choose **Unblock** *(It may
    not be there and that is OK)*

3.  Right click the **FS_Demo_Data.zip** file, and select **Extract All**

4.  Click **Browse**, select a location for the extracted files, click
    **Extract**

5.  Open the **FS_PkgFolder** in the folder on your desktop.

6.  Right click the **DemoDataConfig.xml** file, and select **Edit**

7.  Edit the NewName value to a user in you Dynamics 365 Deployment *(example:
    the user that was created initially when you deployed your trial).* In most
    cases, this will be “**MOD Administrator**”.

8.  **Save and Close** the DemoDataConfig file. **Important:** Before you continue, make sure there is no sample data installed in your Dynamics 365 organization. To ensure there is no sample data:

	- Go to the gear icon in your top menu and click Advanced Settings.

	- Your Business Settings will open in a new window. Click the top drop down
    arrow by Settings to expand the entire settings options.

	- Open Data Management and select Sample Data.

	- If it is installed, select Remove Sample Data before continuing. It may
    take a few minutes to uninstall.

9.  Right click the **PackageDeployer** application in the FieldServiceDemoData
    folder and select **Run as Administrator**

10.  If necessary, click **Yes** on the User Access Control Message

11.  On the Welcome Screen, click **Continue**

12.  Select **Office 365** for the **Deployment Type**

13.  Set the Online Region to your Region, enter your username and password from
    your D365 credentials, and click **Login**

14.  On the **Field Service Demo Data Setup Tool** screen, click **Next**

15.  On the **Ready to Install** Screen, click **Next**

19.  Once the Installer configuration is complete, click **Next**

20.  Wait for the Installer to complete (may take up to 30 or 45 minutes). When
    it is complete, click **Next**

21. Click **Finish** to complete the Field Service Sample Data installation.

Exercise 3 – Map Configuration 
======================================================  

## Task 1 - Enable Bing Maps to use with Resource Scheduling 

To ensure that you are able to take full advantage of the full scheduling and
mapping capabilities available with Field Service, you need to ensure that it is
configured to use a mapping provider.  Bings Maps is the default map provider,
but additional providers could be enabled.  We will be using Bing Maps. 

1.  In **Dynamics 365**, click the arrow next to the **Dynamics 365** text, and
    select **Resource Scheduling**.   

2.  Click the **Site Map** icon in the bottom left corner to
    expand **Navigation**. Click on **Settings.**  From the menu that
    appears, select **Administration**.   

3.  Select **Scheduling Parameters**. 

4.  Locate the **Connect to Maps** field and set it to **Yes**. 

5.  **Save and Close** the settings.   

Exercise 4 - Configure Dynamics 365 for Field Service
=====================================================

In this exercise, you will be modifying and configuring several Field
Service settings that will be used throughout the application. This will
include defining Skills & Certifications, Territories, Resources, and more.

Task 1 - Define Territories
---------------------------

1.  Switch applications from Resource Scheduling to **Field Service.** Click the **Site Map** icon in the bottom left corner to expand
    **Navigation.** Click on **Settings.**

2.  In the left column, click **Territories.**

3.  Click **New**.

4.  Enter **North** for **Name** and click **Save and New**.

5.  Enter **South** for **Name** and click **Save.** After saving, click
    **New**.

6.  Create two more Territories and name them **East** and **West**.

7.  You will now have four additional Territories.

Exercise 5 - Create Service Based product, and Add to Price List 
=================================================================

Task 1 - Add Printer Products
----------------------------

1.  Using the **Sitemap**, select **Products** under **General.**

2.  Click the **Add Product** to create a Product

3.  Define the Details of the Product as noted below:

-   **Name:** Remote Printer

-   **Product ID:** *Print-Serv-1234*

-   **Unit Group:** *Default Unit*

-   **Default Unit:** *Primary Unit*

-   **Decimals Supported:** *2*

1.  Select the **Field Service** tab, set the Field Service Product Type to
    **Inventory**

2.  Set the **Taxable** field to **No**

3.  Save the product, and click **Publish**

4.  Click the **Add Product** to create a Product

5.  Define the Details of the Product as noted below:

-   **Name:** Monthly Printer Maintenance

-   **Product ID:** *Print-Maint4*

-   **Unit Group:** *Default Unit*

-   **Default Unit:** *Primary Unit*

-   **Decimals Supported:** *2*

1.  Select the **Field Service** tab, set the Field Service Product Type to
    **Non-Inventory**

2.  Set the **Taxable** field to **No**

3.  Save the product, and click **Publish**

4.  Click the **Add Product** to create a Product

5.  Define the Details of the Product as noted below:

-   **Name:** Printer Service Fee

-   **Product ID:** *Print-Service-Fee*

-   **Unit Group:** *Default Unit*

-   **Default Unit:** *Primary Unit*

-   **Decimals Supported:** *2*

1.  Select the **Field Service** tab, set the Field Service Product Type to
    **Service**

2.  Set the **Taxable** field to **No**

3.  Save the product, and click **Publish**

Task 2 - Add Printer Products to a Price List
---------------------------------------------

1.  Using the **Sitemap**, select **Price Lists** under **General.**

2.  Open the **Default Price List**

3.  In the **Price List Items**, click the **+ Add** button to add a Price List
    Line Item

4.  Enter the following information:

    1.  **Product:** Remote Printer

    2.  **Unit:** Primary Unit

    3.  **Pricing Method:** Currency Amount

    4.  **Amount:** $1000.00

5.  In the **Price List Items**, click the **+ Add** button to add a Price List
    Line Item

6.  Enter the following information:

    1.  **Product:** Monthly Printer Maintenance

    2.  **Unit:** Primary Unit

    3.  **Pricing Method:** Currency Amount

    4.  **Amount:** $750.00

7.  Click **Save and Close**

8.  In the **Price List Items**, click the **+ Add** button to add a Price List
    Line Item

9.  Enter the following information:

    1.  **Product:** Printer Service Fee

    2.  **Unit:** Primary Unit

    3.  **Pricing Method:** Currency Amount

    4.  **Amount:** $150.00

10. Click **Save and Close**

11. Close the Default Price List

