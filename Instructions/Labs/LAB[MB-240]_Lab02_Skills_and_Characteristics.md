---
lab:
    title: 'Lab 2: Skills and characteristics (20 minutes)'
    module: 'Module 1: Configure Field Service'
---

# Practice Lab 2 - Skills and characteristics

## Exercise 1 - Configure Dynamics 365 for Field Service Skills and Characteristics

Each technician that goes out to service customers may have a number of different skills and roles assigned to them. There are three primary roles that tech may have:

- Installation Specialist
- Site Inspector
- Security Analyst

Additionally, each technician may have specific skills or Certifications that relate to a specific product or service. The most common certifications might be any of the following:

- **CISM:** Certified Information Security Manager
- **CISSP:** Certified Information Systems Security Professional
- **G SEC:** GIAN Security Essentials

Since some of your customers are government agencies, technicians may need to have specific security clearance levels. These can range from Level one to Level five.

### Task 1 – Proficiency Models

In this task you will create a proficiency model that contains the five different security clearance levels and a proficiency model for skill level.

1. In the **Dynamics 365 Field Service app**, click the **Resources** area in the bottom-left of the sitemap, and in the **Resource** group select **Proficiency Models**.

1. Click **+ New** located on the command bar.

1. Enter **[your prefix ex. mollyc]** + **Security Level** for **Name**.

1. Enter **1** for **Min Rating Value**.

1. Enter **5** for **Max Rating Value**.

1. Click **Save**.

1. If Rating Values are not shown in a sub-gird on the General tab, click **Related** and select **Rating Values**.

1. Click **+ New Rating Value**.

1. Enter **[your prefix ex. mollyc]** + **Level 1 Security** for **Name**.

1. Enter **1** for **Value**.

1. Click **Save & Close**.

1. Click **+ New Rating Value**.

1. Enter **[your prefix ex. mollyc]** + **Level 2 Security** for **Name**.

1. Enter **2** for **Value**.

1. Click **Save & Close**.

1. Click **+ New Rating Value**.

1. Enter **[your prefix ex. mollyc]** + **Level 3 Security** for **Name**.

1. Enter **3** for **Value**.

1. Click **Save & Close**.

1. Click **+ New Rating Value**.

1. Enter **[your prefix ex. mollyc]** + **Level 4 Security** for **Name**.

1. Enter **4** for **Value**.

1. Click **Save & Close**.

1. Click **+ New Rating Value**.

1. Enter **[your prefix ex. mollyc]** + **Level 5 Security** for **Name**.

1. Enter **5** for **Value**.

1. Click **Save & Close**.

1. Click **Save & Close**.

1. In the **Dynamics 365 Field Service app**, click the **Resources** area in the bottom-left of the sitemap, and in the **Resource** group select **Proficiency Models**.

1. Click **+ New** located on the command bar.

1. Enter **[your prefix ex. mollyc]** + **Proficiency** for **Name**.

1. Enter **1** for **Min Rating Value**.

1. Enter **3** for **Max Rating Value**.

1. Click **Save**.

1. If Rating Values are not shown in a sub-gird on the General tab, click **Related** and select **Rating Values**.

1. Click **+ New Rating Value**.

1. Enter **[your prefix ex. mollyc]** + **Familiar** for **Name**.

1. Enter **1** for **Value**.

1. Click **Save & Close**.

1. Click **+ New Rating Value**.

1. Enter **[your prefix ex. mollyc]** + **Proficient** for **Name**.

1. Enter **2** for **Value**.

1. Click **Save & Close**.

1. Click **+ New Rating Value**.

1. Enter **[your prefix ex. mollyc]** + **Expert** for **Name**.

1. Enter **3** for **Value**.

1. Click **Save & Close**.

1. Click **Save & Close**.

### Task 2 - Define a Security Clearance skill

In this task you will create a building security skill that will be used in conjunction with the Proficiency Model you defined in the previous task.

1. Click on the name of the app in the top left of the application next to Dynamics 365 and from the list of published apps, select the **Resource Scheduling** app.

1. In the **Resource Scheduling app**, click the **Settings** area in the bottom-left of the sitemap, and in the **Resource** group select **Skills**.

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **Building Security** for **Name**.

1. Select **Skill** from the **Characteristic Type** drop-down field.

1. Click **Save & Close**.

### Task 3 - Define Security certifications

In this task you will be adding the **CISM:** Certified Information Security Manager, **CISSP:** Certified Information Systems Security Professional, and **GSEC:** GIAN Security Essentials certifications and resource skills.

1. In the **Resource Scheduling app**, click the **Settings** area in the bottom-left of the sitemap, and in the **Resource** group select **Skills**.

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **CISM** for **Name**.

1. Enter **[your prefix ex. mollyc]** + **Certified Information Security Manager** for **Description**.

1. Select **Certification** from the **Characteristic Type** drop-down field.

1. Click **Save & Close**.

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **CISSP** for **Name**.

1. Enter **[your prefix ex. mollyc]** + **Certified Information Systems Security Professional** for **Description**.

1. Select **Certification** from the **Characteristic Type** drop-down field.

1. Click **Save & Close**.

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **G SEC** for **Name**.

1. Enter **[your prefix ex. mollyc]** + **GIAC Security Essentials** for **Description**.

1. Select **Certification** from the **Characteristic Type** drop-down field.

1. Click **Save & Close**.

### Task 4 - Define Resource Roles (Categories)

In this task, you will be adding the Installation Specialist, Site Inspector, and Security Analyst resource roles.

1. In **Resource Scheduling app**, click the **Settings** area in the bottom-left of the sitemap, and in the **Resource** group select **Roles**.

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **Installation Specialist** for **Name**.

1. Enter **Installation Specialist** for **Description**.

1. Click **Save & Close**.

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **Site Inspector** for **Name**.

1. Enter **Site Inspector** for **Description**.

1. Click **Save & Close**.

1. Click **+ New**.

1. Enter **[your prefix ex. mollyc]** + **Security Analyst** for **Name**.

1. Enter **Security Analyst** for **Description**.

1. Click **Save & Close**.

1. Click on the name of the app in the top left of the application next to Dynamics 365 and from the list of published apps, select the **Field Service** app.

1. Navigate to **Resources** -> **Resource** -> **Categories**.

1. Verify the roles you created are listed under Active Resource Categories.
