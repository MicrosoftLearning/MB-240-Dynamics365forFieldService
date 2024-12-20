---
lab:
    title: 'Lab 1: Configure Field Service (10 minutes)'
    module: 'Module 1: Configure Field Service'
---

# Practice Lab 1 - Configure Dynamics 365 Field Service

## Scenario

Contoso Coffee produces high-quality coffee and coffee machines. Their products are sold through retail channels including new Contoso retail stores in premium locations, premium food resellers and the Contoso Coffee Web Site. Even though their products are sold through different channels, they have certified technicians that either work directly for Contoso Coffee, or that work for authorized service providers. 

Contoso coffee will be leveraging Dynamics 365 for Field Service to help manage machine installation for commercial vendors, and servicing machines for commercial and retail customers. You are the system implementor who has been tasked with configuring the Dynamics 365 Field service to support their rollout of the application. 

Contoso wants to leverage the Dynamics 365 product catalog to define the products and services that will be delivered on work orders.  Additionally, Contoso splits their service zones into territories to make it easier to schedule onsite workers. You have been asked to configure the system to support these needs. 

Upon successful completion of this lab, you will have successfully configured the following:
* Ensured that Bing Maps can be used with resource scheduling.
* Defined the different territories boundaries required.
* Defined the Products and Services that will be delivered in the Product Catalog. 


## Exercise 1 – Map Configuration

### Task 1 - Enable Bing Maps to use with Resource Scheduling

To ensure Contoso can take full advantage of all the scheduling and mapping capabilities available with Dynamics 365 Field Service, you need to ensure that it is configured to use a mapping provider. Bing Maps is the default map provider, but additional providers could be enabled. For the purposes of this exercise, we will be using Bing Maps.

1. In the **Dynamics 365 Field Service app**, click the **Resources** area in the bottom-left of the sitemap, and in the **Administration** group select **Scheduling Parameters**.

1. Open the **Resource Scheduling** record.

1. Locate the **Connect to Maps** field. This should be set to **Yes**.

1. If **Connect to Maps** is set to **No**, set it to **Yes** and click **OK** from the popup.

1. Click **Save and Close**.

## Exercise 2 - Configure Territories

As mentioned previously, Contoso breaks the areas that they service into different territories. In this exercise, you will define the territories that will later be associated with Contoso’s different resources and work orders.

### Task 1 - Define Territories

1. In the **Dynamics 365 Field Service app**, click the **Settings** area in the bottom-left of the sitemap, and in the **General** group select **Territories**.

1. Click **+ New** located on the command bar.

1. Enter **North** for **Territory Name** and click **Save**. Click **+ New**.

1. Enter **South** for **Territory Name** and click **Save**. Click **+ New**.

1. Enter **East** for **Territory Name** and click **Save**. Click **+ New**.

1. Enter **West** for **Territory Name** and click **Save & Close**.

1. You will now have four Territories with your prefix.

## Exercise 3 - Create Products

When onsite workers are servicing customers, they will often be installing, or replacing parts on different machines. Contoso wants to be able to track the products being installed, as well as the different services an onsite worker might provide. 
You will need to add different products and services to the Dynamics 365 Product Catalog to support this. 

### Task 1 - Add Inventory Product

1. In the **Dynamics 365 Field Service app**, click the **Settings** area in the bottom-left of the sitemap, and in the **General** group select **Products**.

1. Click **Add Product**.

1. Enter **Remote Printer** for **Name**.

1. Enter **Print-Serv-1234** for **Product ID**.

1. Select **Default Unit** for **Unit Group**.

1. Select **Primary Unit** for **Default Unit**.

1. Set **Decimals Supported** to **2**.

1. Select the **Field Service** tab.

1. Set **Field Service Product Type** to **Inventory**.

1. Click **Save**. (You may see a warning that a default price list has not been set. You can ignore this.)

1. Click **Publish** and click **Confirm** from the popup.

1. Click **Save & Close**

### Task 2 - Add Non-Inventory Product

1. Click **Add Product**.

1. Enter **Monthly Printer Maintenance** for **Name**.

1. Enter **Print-Maint** for **Product ID**.

1. Select **Default Unit** for **Unit Group**.

1. Select **Primary Unit** for **Default Unit**.

1. Set **Decimals Supported** to **2**.

1. Select the **Field Service** tab.

1. Set **Field Service Product Type** to **Non-Inventory**.

1. Click **Save**. (You may see a warning that a default price list has not been set. You can ignore this.)

1. Click **Publish** and click **Confirm** from the popup.

1. Click **Save & Close**

### Task 3 - Add Service Product

1. Click **Add Product**.

1. Enter **Printer Service Fee** for **Name**.

1. Enter **Printer-Service-Fee** for **Product ID**.

1. Select **Default Unit** for **Unit Group**.

1. Select **Primary Unit** for **Default Unit**.

1. Set **Decimals Supported** to **2**.

1. Select the **Field Service** tab.

1. Set **Field Service Product Type** to **Service**.

1. Click **Save**. (You may see a warning that a default price list has not been set. You can ignore this.)

1. Click **Publish** and click **Confirm** from the popup.

1. Click **Save & Close**

### Task 4 - Add Products to a Price List

1. In the **Dynamics 365 Field Service app**, click the **Settings** area in the bottom-left of the sitemap, and in the **General** group select **Price Lists**.

1. Click **+ New**.

1. Enter **Price List** for **Name**.

1. Click **Save**.

1. Select the **Price List Items** tab.

1. Click **+ New Price List Item**.

1. Select the **Remote Printer** product you created in Task 1.

1. Select **Primary Unit** for **Unit**.

1. Select the **Pricing Information** tab.

1. Select **Currency Amount** from the **Pricing Method** drop-down field.

1. Enter **1000.00** for **Amount**.

1. Click **Save & Close**.

1. Click **+ New Price List Item**.

1. Select the **Monthly Printer Maintenance** product you created in Task 2.

1. Select **Primary Unit** for **Unit**.

1. Select the **Pricing Information** tab.

1. Select **Currency Amount** from the **Pricing Method** drop-down field.

1. Enter **750.00** for **Amount**.

1. Click **Save & Close**.

1. Click **+ New Price List Item**.

1. Select the **Printer Service Fee** product you created in Task 3.

1. Select **Primary Unit** for **Unit**.

1. Select the **Pricing Information** tab.

1. Select **Currency Amount** from the **Pricing Method** drop-down field.

1. Enter **150.00** for **Amount**.

1. Click **Save & Close**.

1. Click **Related** on the Price List and select **Field Service Price List Items**.

1. Click **+ New Field Service Price List Item**.

1. Enter **Printer Service Fee** for **Name**.

1. Select **Yes** from the **Flat Fee** drop-down field.

1. Select the **Price List** price list you created in Task 4.

1. Select the **Printer Service Fee** product you created in Task 3.

1. Click **Save & Close**.
