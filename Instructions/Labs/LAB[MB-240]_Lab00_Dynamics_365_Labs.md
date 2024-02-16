---
lab:
    title: 'Lab 0: Validate lab environment (5 minutes)'
    module: 'Module 0: Course introduction'
---

# Practice Lab - Validate lab environment

## Scenario

Contoso Coffee produces high-quality coffee and coffee machines. They sell their products through retail channels including new Contoso retail stores in premium locations, premium food resellers and the Contoso Coffee website. Even though their products are sold through different channels, they have certified technicians that either work directly for Contoso Coffee, or that work for authorized service providers who they use to provide service on machines. 

Contoso coffee will be leveraging Dynamics 365 for Field Service to help manage machine installations at commercial vendors, as well as for servicing machines for commercial and retail customers. You are the system implementor who has been tasked with configuring the Dynamics 365 Field service to support their rollout of the application. 

You will be the primary person who will be configuring the key elements of Contoso Coffees field service deployment. 

This will include the following:

* Setting up initial system settings configurations. 
* Defining product and services.
* Configuring resources that will be assigned to jobs.
* Configuring the system to deliver and manage work orders. 
* Setting the schedule board to schedule work orders.
* Configuring agreements.
* Setting up customer assets. 


In this Module 0 lab, you will validate that your classroom tenant is working as expected. You will access your individual credentials, record your “*alias*,” and open the Dynamics 365 model-driven application that we will be using throughout the course.

**Important notice for instructors:** Please do not make any changes, including adding licenses or changing tenant password. Tenants are fully provisioned with all necessary licenses, environments, and applications to complete the required tenants. Instructors and students should not add any additional functionality outside of the published lab steps. Adding additional functionality will cause the tenant to break and become inactive, and changing the tenant password will inhibit the recycling of the tenant for the next class. Thank you for your cooperation.

**Important Note:** This lab will provide you with an actual Dynamics 365 tenant and licenses for the Power Platform applications you will be using in this course. Please be aware that the Power Platform is evolving all the time. The instructions in this document may be different from what you experience in your actual tenant. It is also possible to experience a delay of several minutes before the virtual machine has network connectivity to begin the labs.


## Exercise 1 - Access the Dynamics 365 application

### Task 1 – Log into the Power Platform admin center

1. In a new browser, navigate to the Power Platform admin center `https://aka.ms/ppac` and sign in with your Dynamics 365 tenant credentials.

1. Record your user credential up to the **@** symbol on a scratch piece of paper or in Notepad. This will be your lab alias that you will use to differentiate the data you create within the shared Dynamics 365 organization.

**Important:** Please be aware that this tenant and the Dynamics 365 organization will be shared with the other students in your classroom, like employees would share a tenant when using the Dynamics 365 instance belonging to their organization. Do not use any PII (personally identifiable information) when creating records. It is also good practice to use your user's prefix (ex., **mollyc**) in front of all records, data, apps, flows, etc. that you create.

1. Feel free to explore the Power Platform admin center but **do not make any changes**.


### Task 2 – Access the Dynamics 365 application

1. In the Power Platform admin center, select **Environments** <https://admin.powerplatform.microsoft.com/environments>.

1. Select the **WWLCLOUDCEnnnnnn** environment, where nnnnnn is a number. This is the shared Dynamics 365 environment where you will be performing all labs.

1. Select **Open**.

1. From the list of available Dynamics 365 apps, select the **Field Service** app.

1. Spend a few minutes exploring the application.
