---
lab:
    title: 'Lab: Agreements'
    module: 'Module 2: Manage Work Orders'
---

# Practice Lab 6 - Agreements

## Exercise 1 - Create an Agreement

In this exercise you will be defining a preventative maintenance agreement that will generate Work orders monthly and bill customers quarterly.

### Task 1 - Create Agreement

1. In the **Dynamics 365 Field Service app**, click the **Service** area in the bottom-left of the sitemap, and in the **Service Delivery** group select **Agreements**.

1. Click **+ New**.

1. Select the **[your prefix] Relecloud** account you created in a previous lab for **Service Account**.

1. Select the **[your prefix] Price List** price list you created in a previous lab for **Price List**.

1. Select **No** from the **Taxable** drop-down field.

1. Select the first of the current month for the **Start Date**.

1. Select the **End Date** to 12 months after the start date.

1. Set **Duration** to **365 days**.

1. Click **Save**.

### Task 2 - Setup an Automated Booking for the Agreement

1. In the agreement created in Task 1, click on the ellipsis (...) in the **Booking Setup** section, and select **+ New Agreement Booking Setup**.

1. Enter **[your prefix ex. mollyc]** + **Monthly Printer Service** for **Name**.

1. Select **Yes** for **Auto Generate Work Order**.

1. Select **60** for **Auto Generate Work Order Days in Advance**.

1. Select the **[your prefix] Low** priority you created in a previous lab for **Priority**.

1. Select the **[your prefix] Price List** price list you created in a previous lab for **Price List**.

1. Select **No** for **Auto Generate Work Booking**.

1. Select **1 Hour** for **Estimated Duration**.

1. Select **3** for **Pre Booking Flexibility**.

1. Select **3** for **Post  Booking Flexibility**.

1. Select **9:00 AM** for **Time Window Start**.

1. Select **12:00 PM** for **Time Window End:**.

1. Click **Save**.

1. Click on the ellipsis (...) in the **Incidents** section, and select **+ New Agreement Booking Incident**.

1. Select the **[your prefix] Service Printer** incident type you created in a previous lab for **Incident Type**.

1. Click **Save and Close**.

1. Click **Booking Recurrence** in the command bar.

1. Select **Monthly** from **Repeat** drop-down list.

1. Select **End after (#specified) occurrences** from **End Date Behavior** drop-down list.

1. Enter **12** for **Number of occurrences**.

1. Click **OK**.

1. Click **Save & Close**.

1. In the business process flow, click **Next Stage** and select the Agreement Booking Setup.

### Task 3 - Setup an Automated Invoice for the Agreement

1. In the agreement created in Task 1, click on the ellipsis (...) in the **Invoice Setup** section, and select **+ New Agreement Invoice Setup**.

1. Enter **[your prefix ex. mollyc]** + **Quarterly Invoice** for **Name**.

1. Click **Save**.

1. Select the **Invoice Products** tab.

1. Click **+ New Agreement Invoice Product**.

1. Select the **[your prefix] Monthly Printer Maintenance** product you created in a previous lab for **Product**.

1. Select the **Primary Unit** for **Unit**.

1. Select the **Quantity & Sale Amount** tab.

1. Enter **3** for **Quantity**.

1. Click **Save & Close**.

1. Click **Save & Close**.

1. In the business process flow, click **Next Stage** and select the Agreement Invoice Setup.

1. In the business process flow, click **Next Stage**.

### Task 4 - Generate work orders

1. Return to the agreement created in Task 1.

1. Select **Active** from the **System Status** drop-down field.

1. Click **Save**.

1. In the **Booking Setup** section, open the Agreement Booking Setup you created in Task 2.

1. Verify there are booking dates listed.
