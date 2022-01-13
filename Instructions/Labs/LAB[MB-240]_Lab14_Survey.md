---
lab:
  title: 'Lab 14: Create survey (25 minutes)'
  module: 'Module 7: Power Platform'
---

# Practice Lab 14 – Customer Voice

## Scenario

You are a dispatch manager at Relecloud who has been tasked with trying the Customer Voice functionality to capture feedback on work orders before rolling it out to your customers.

## Exercise 1: Create survey

In this exercise, you will create a project and use a template to create a survey.

### Task 1: Create project

1. Navigate to <https://customervoice.microsoft.com>.

1. Sign in with your Dynamics 365 tenant credentials.

1. Create a new Project.

1. Select the **Service visit** template

1. Click **Next**

1. Select the **WWLLABnnn** Dynamics 365 environment. If the environment is not listed, click **See all environments**.

1. Click **Create**.

1. Click on **All Projects**

1. Click on the ellipsis next your project and select **Rename**.

1. Enter **[your prefix ex. mollyc]** + **Work Order Visit Feedback** and click on **Rename**.

### Task 2: Customize survey

1. Select your project.

1. Click in the **Header** and change **Field service feedback** to **How did we do?**.

1. Hover the mouse over the header and click on the **Theme color** icon and change from 2266e3 to **ffdd66**.

1. Hover the mouse over the header and click on the **Image** icon and choose one of the images from the gallery.

1. Select question 1 and set as **Required**.

1. Select question 2 and set as **Required**.

1. After the second question in the survey and click on **+ Add new** and click on the chevron(V) and select the **Net Promoter Score** question type. Set the question as **Required**.

1. Click on **Post-survey message** and change the Heading from *Thanks!* to **Thank you for your feedback** and change the Message to **We look at all feedback to improve our service.**

1. Click in the Footer and enter **The feedback you submit will not be shared outside of the company.**

1. Expand **Customization** and select **Personalization**.

1. Click + **Add variable** and enter **workordernumber** with default value **your booking**.

1. Click **Save**.

1. Click **Close**.

1. Select **Formatting**

1. Toggle **Progress bar** to **Off** and close the formatting pane.

1. Click into the section header that starts with *Hi {{First Name}}* and clear the text *it*, click on the **variables** drop-down and select **workordernumber**.

1. Click **Preview**.

1. Click **Back**.

### Task 3: Satisfaction metrics

1. Select your survey.

1. Expand **Customization** and select **Satisfaction metrics**

1. Click **+ Add metric**

1. Select **Net Promoter Score** and select the third question.

1. Click **Save**.

1. Click **Cancel**

## Exercise 2: Send survey

In this exercise, you will create an email template and send the survey by email.

### Task 1: Configure email template

1. Navigate to <https://customervoice.microsoft.com>

1. Select your project.

1. Select your survey.

1. Click on the **Send** tab.

1. Click on the **Email** tile.

1. Click on the **Template** drop-down and select **Create new**.

1. Enter **[your prefix ex. mollyc]** + **Field Service Visit** and click **Add**.

1. Click on the **Template** drop-down and **[your prefix] Field Service Visit**.

1. Click in the top of the body of the email template.

1. Click on the **Insert** drop-down and select **First question of the survey**.

1. Replace the subject line with **Please provide feedback on**, click on the **Insert** drop-down and select **Personalized variables** and then select **workordernumber**.

1. Click **Save**

1. Click **Cancel**

### Task 2: Send the survey

1. Click on the **Send** tab.

2. Click on the **Email** tile.

3. Click on the **Template** drop-down and select the **Field Service Visit** template you created.

4. Click in the Recipients field and enter your email address.

5. Click **Send**

## Exercise 3: Send survey when a work order is completed

In this exercise, you will use Power Automate to send a survey when a work order is completed.

### Task 1: Configure automation

1. Navigate to <https://customervoice.microsoft.com>

1. Select your project.

1. Select your survey.

1. Click on the **Send** tab.

1. Click on **Resend** and select **Automate**.

1. Select the **Send a survey when a work order is completed or closed in Dynamics 365** template. You may need to click on **See more templates**.

1. If the connections require action, click **Fix connection** and **Sign in** when prompted.

1. Click **Continue**.

1. Expand the steps in the flow and select the send a survey step.

1. Clear the **Email** template field and select the **Field Service Visit** template you created.

1. Click **Save**.
