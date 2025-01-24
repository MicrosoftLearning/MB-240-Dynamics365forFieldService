---
lab:
    title: 'Lab 7: Inspections (15 minutes)'
    module: 'Module 2: Manage Work Orders'
---

# Practice Lab 7 - Inspections
## Scenario
When Contoso’s technicians are performing preventative maintenance work orders, Contoso wants to ensure that all technicians are following the same inspection process. This Process ensures that nothing is missed.   

This inspection process includes: 
- Identifying the make and model of the machine are inspecting. 
- Taking a temperature and pressure reading.
- Descaling or replacing the brew sensor as needed. 
- Taking a picture of the controller assembly.
- Logging the date, they performed the inspection on. 
- Add any relevant notes. 

The inspection should be associated with an Inspection task on the preventative Maintenance incident type. 

## Exercise 1 - Create and use an Inspection Template

In this exercise you will be defining an inspection template, adding it to an inspection service type task, and ensuring the task is on the Preventative Maintenance incident type. 

### Task 1 - Create Inspection Template

1. In the **Dynamics 365 Field Service app**, click the **Settings** area in the bottom-left of the sitemap, and in the **Work Orders** group select **Inspection Templates**.

1. Click **+ New**.

1. Enter **Printer Inspection** for **Name for Inspection**.

1. Click on **TextBox** to add question.

1. Enter **Serial number** for **Question1** title.

1. Toggle **Required** to On.

1. Click **Advanced**.

1. Select **Barcode** for **Input type**.

1. Select **Toolbox** tab.

1. Click on **Dropdown** to add question.

1. Enter **Condition** for **Question2** title.

1. Toggle **Required** to On.

1. Change **Item 1** to **Poor**.

1. Change **Item 2** to **Satisfactory**.

1. Change **Item 3** to **Good**.

1. Click on **Number** to add question.

1. Enter **Page Count** for **Question3** title.

1. Select the **Advanced** tab.

1. Toggle **Whole Number** to On.

1. Select the **Toolbox** tab.

1. Click on **TextBox** to add question.

1. Enter **Comments** for **Question4** title.

1. Select the **Advanced** tab.

1. Select **MultiLine** for the **Input type** drop-down.

1. Select the **Toolbox** tab.

1. Click on **File** to add question.

1. Enter **Image** for **Question5** title.

1. Click the **Preview** tab.

1. Click **Save**.

1. Click **Publish** and click **Publish** again.

### Task 2 - Add Inspection Template to Service Type Task

1. In the **Dynamics 365 Field Service app**, click the **Settings** area in the bottom-left of the sitemap, and in the **Work Orders** group select **Service Task Types**.

1. Click **+ New**.

1. Enter **Inspect Printer** for **Name**.

1. Enter **15 Minutes** for **Estimated Duration**.

1. Toggle **Has Inspection** to **Yes**.

1. Select the **Printer Inspection** inspection template you created in Task 1 for **Inspection Template**.

1. Click **Save**.

1. In the **Dynamics 365 Field Service app**, click the **Settings** area in the bottom-left of the sitemap, and in the **Work Orders** group select **Incident Types**.

1. Edit the **Service Printer** incident type.

1. Select the **Service Tasks** tab.

1. Click **+ New Incident Type Service Task**.

1. Enter **Inspect Printer** for **Name**.

1. Select the **Inspect Printer** service task type you created in Task 2 for **Task Type**.

1. Click **Save and Close**.

1. Click **Save & Close**.

### Task 3 – Download an image

1. In the browser, open Microsoft Bing and do an image search for printers. 

1. Right click on the image of the printer and select **Save image as** and click **Save**.

### Task 4 – Create a new Work Order and view the inspection

1. In the **Dynamics 365 Field Service app**, click the **Service** area in the bottom-left of the sitemap, and in the **Scheduling** group select **Work Orders**.

1. Click **+ New**.

1. Select the **Relecloud** account you created in Task 1 for **Service Account**.

1. Select the **Service Printer** incident type you created in a previous lab for **Primary Incident Type**.

1. Click **Save**.

1. Wait about 30 seconds to a minute and click **Refresh** in the command bar.

1. Select the **Service Tasks** tab and verify that the four tasks were added.

1. Open the **Inspect Printer** work order service task.

1. Enter **122333** for **Serial number**.

1. Select **Satisfactory** from the **Condition** drop-down field.

1. Enter **999** for **Page Count**.

1. Enter **No problems found** for **Comments**.

1. Click on **Choose file(s)** and browse to the image you downloaded in Task 3 and click **Open**.

1. Click **Save**.

1. Select **Pass** for **Result**.

1. Click **Mark Complete**.
