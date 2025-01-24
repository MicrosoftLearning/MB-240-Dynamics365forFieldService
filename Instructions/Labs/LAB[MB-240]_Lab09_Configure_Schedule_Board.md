---
lab:
    title: 'Lab 9: Configure Schedule Boards (10 minutes)'
    module: 'Module 3: Schedule and dispatch work orders'
---

# Practice Lab 9 - Configure the Schedule Board
## Scenario
Contoso Coffee’s dispatchers are telling you that there are too many resources when trying to schedule items using the schedule board. They feel like it would be easier to schedule resources if the schedule boards were broken down into a series of smaller boards. One way they have identified to simplify scheduling is to have different boards broken down by territory.

Each board should include the following:
- Unscheduled work orders should only include work orders for that territory. 
- Listed resources should only be resources associated with that territory.

It is important to note that some resources might be assigned to multiple territories. It is OK if they show up on multiple schedule boards. 

## Exercise 1 - Create and configure a new schedule board

In this exercise we will create and configure a schedule board for the WA territory.

Successful configuration will include:   
- Creation/Modification of necessary views based on territory. 
- Creation of WA schedule board.
- Filtering the board based on different views. 


### Task 1 – Create a schedule board

1. In the **Dynamics 365 Field Service app**, click the **Service** area in the bottom-left of the sitemap, and in the **Scheduling** group select **Schedule Board**.

1. Click the **+** icon in the top-left of the schedule board to add a new schedule board tab.

1. Enter **Board** for **Board Name**.

1. Select **Everyone** from the **Shared with** drop-down field.

1. Select the **Schedule Assistant** tab.

1. Enter **c6fcb3** for **Available color**.

1. Select **Start of travel** from the **Book based on** drop-down field.

1. Select the **Board colors** tab.

1. Enter **c6fcb3** for **Not booked**.

1. Enter **bf2626** for **Current timeline**.

1. Select the **Other** tab.

1. Enter **10** for **Requirement page count**.

1. Enter **12** for **Resource page count**.

1. Click **Add**.

1. Select the  **Board** tab.

1. Click on the **Scheduler Settings** gear icon on the Schedule Board.

1. Select your **Time Zone**.

1. Select **8:00 AM to 6:00 PM** for **Working time**.

1. Select **30 minutes** for **Time resolution**.

1. Click on the **Filters** icon.

1. Select **User** from the **Resource Types** drop-down field.

1. Click **Apply**.

1. Click **Save as default**.

1. Close the **Filters** pane.
