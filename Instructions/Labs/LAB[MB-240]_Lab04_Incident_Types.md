---
lab:
    title: 'Lab 4: Incident types (15 minutes)'
    module: 'Module 2: Manage Work Orders'
---

# Practice Lab 4 - Incident types

## Exercise 1 – Create an Incident Type

In this exercise you will create and populate an Incident Type as a template for creating work orders.

### Task 1 - Work Order Type

1. In the **Dynamics 365 Field Service app**, click the **Settings** area in the bottom-left of the sitemap, and in the **Work Orders** group select **Work Order Types**.

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **Service Call** for **Name**.

1. Select **Yes** from the **Incident Required** drop-down field.

1. Select **No** from the **Taxable** drop-down field.

1. Select the **[your prefix] Price List** record you created in the previous lab for **Price List**.

1. Click **Save & Close**

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **Inspection** for **Name**.

1. Select **No** from the **Incident Required** drop-down field.

1. Select **No** from the **Taxable** drop-down field.

1. Select the **[your prefix] Price List** record you created in the previous lab for **Price List**.

1. Click **Save & Close**

### Task 2 – Service Task Types

1. In the **Dynamics 365 Field Service app**, click the **Settings** area in the bottom-left of the sitemap, and in the **Work Orders** group select **Service Task Types**.

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **Clean Printer Assembly** for **Name**.

1. Select **30 Minutes** for **Estimated Duration**.

1. Click **Save and Close.**

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **Replace Toner** for **Name**.

1. Select **15 Minutes** for **Estimated Duration**.

1. Click **Save and Close.**

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **Final Test** for **Name**.

1. Select **15 Minutes** for **Estimated Duration**.

1. Click **Save and Close.**

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **Inspection** for **Name**.

1. Select **45 Minutes** for **Estimated Duration**.

1. Click **Save and Close.**

### Task 3 – Incident Type

1. In the **Dynamics 365 Field Service app**, click the **Settings** area in the bottom-left of the sitemap, and in the **Work Orders** group select **Incident Types**.

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **Service Printer** for **Name**.

1. Select the **Details** tab.

1. Select the **[your prefix] Service Call** work order type you created in Task 1 for **Default Work Order Type**.

1. Select **Yes** from the **Copy Incident Items to Agreement** drop-down field.

1. Click **Save**.

1. Select the **Service Tasks** tab.

1. Click **+ New Incident Type Service Task**.

1. Enter **[your prefix ex. mollyc]** + **Clean Printer Assembly** for **Name**.

1. Select the **[your prefix] Clean Printer Assembly** service task type you created in Task 2 for **Task Type**.

1. Click **Save and Close**.

1. Click **+ New Incident Type Service Task**.

1. Enter **[your prefix ex. mollyc]** + **Replace Toner** for **Name**.

1. Select the **[your prefix] Replace Toner** service task type you created in Task 2 for **Task Type**.

1. Click **Save and Close**.

1. Click **+ New Incident Type Service Task**.

1. Enter **[your prefix ex. mollyc]** + **Final Test** for **Name**.

1. Select the **[your prefix] Final Test** service task type you created in Task 2 for **Task Type**.

1. Click **Save and Close**.

1. Select the **Products** tab.

1. Click **+ New Incident Type Product**.

1. Enter **[your prefix ex. mollyc]** + **Remote Printer** for **Name**.

1. Select the **[your prefix] Remote Printer** product you created in a previous lab for **Product**.

1. Select the **Primary Unit** for **Unit**.

1. Enter **1** for **Quantity:**.

1. Click **Save and Close**.

1. Select the **Services** tab.

1. Click **+ New Incident Type Service**.

1. Enter **[your prefix ex. mollyc]** + **Printer Service Fee** for **Name**.

1. Select the **[your prefix] Printer Service Fee** product you created in a previous lab for **Service**.

1. Select the **Primary Unit** for **Unit**.

1. Click **Save and Close**.

1. Select the **Characteristics** tab.

1. Click **+ New Incident Type Characteristic**.

1. Select the **[your prefix] CISM** characteristic you created in a previous lab for **Characteristic**.

1. Select the **[your prefix] Familiar** rating you created in a previous lab for **Rating Value**.

1. Click **Save and Close**.

1. Select the **Characteristics** tab.

1. Click **+ New Incident Type Characteristic**.

1. Select the **[your prefix] Building Security** characteristic you created in a previous lab for **Characteristic**.

1. Select the **[your prefix] Level 2 Security** rating you created in a previous lab for **Rating Value**.

1. Click **Save and Close**.

## Exercise 2 – Test the Incident Type

In this exercise you will create a work order by using the incident type.

### Task 1 - Create Customer

1. In the **Dynamics 365 Field Service app**, click the **Service** area in the bottom-left of the sitemap, and in the **Customers** group select **Accounts**.

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **Relecloud** for **Account Name**. Click **Save**.

1. Click **Save & Close**.

1. Click on **Contacts** in the **Customers** group of the sitemap.

1. Click **+ New** located on the command bar.

1. Enter **[your prefix ex. mollyc]** + **Jane** for **First Name**.

1. Enter **Doe** for **Last Name**.

1. Select the **[your prefix] Relecloud** account you created in Task 1 for **Account Name**.

1. Click **Save & Close**.

### Task 2 – Create a new Work Order using an Incident Type

1. In the **Dynamics 365 Field Service app**, click the **Service** area in the bottom-left of the sitemap, and in the **Scheduling** group select **Work Orders**.

1. Click **+ New**.

1. Select the **[your prefix] Relecloud** account you created in Task 1 for **Service Account**.

1. Select the **[your prefix] Service Call** you created in a previous lab for **Work Order Type**.

1. Select **No** from the **Taxable** drop-down field.

1. Select the **[your prefix] Service Printer** incident type you created in a previous lab for **Primary Incident Type**.

1. Click **Save**.

1. Wait about 30 seconds to a minute and click **Refresh** in the command bar.

1. Select the **Products** tab and verify that the **[your prefix] Remote Printer Product** was added.

1. Select the **Services** tab and verify that the **[your prefix] Printer Service Fee** was added.

1. Select the **Service Tasks** tab and verify that the three tasks were added.

1. Click **Related** and select **Characteristics**.

1. Verify that the two Characteristics defined on the Incident Type were added.
