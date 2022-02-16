# Teams Adaptive Card Reminders From Lists

## Summary

This sample will send a *Microsoft Teams* adaptive card reminder from *Microsoft Lists* to the item owner in advance of the due date using *Power Automate*.

![Flow overview](/samples/teams-adaptive-card-reminders-from-lists/assets/flow-overview.png "Flow overview")


## Applies to

* [Microsoft Power Automate](https://docs.microsoft.com/power-automate/)


## Compatibility

![Premium License](https://img.shields.io/badge/Premium%20License-Not%20Required-green.svg "Premium license not required")
![On-Premises Connectors](https://img.shields.io/badge/On--Premises%20Connectors-No-green.svg "Does not use on-premise connectors")
![Custom Connectors](https://img.shields.io/badge/Custom%20Connectors-Not%20Required-green.svg "Does not use custom connectors")


## Authors

Solution|Author(s)
--------|---------
teams-adaptive-card-reminders-from-lists | [Norm Young](https://github.com/nyoung30) ([@stormin_30](https://twitter.com/stormin_30))


## Version history

Version|Date|Comments
-------|----|--------
1.0|February 16, 2022|Initial release


## Features

This sample illustrates the following concepts:

* OData filter queries
* Expressions
* Adaptive cards


## Prerequisites

This Flow requires the following list columns and settings:
* **Title**
	* Settings: "Require that this column contains information" set to **Yes**
* **DueDate**
	* Type: *Date time* with "Include time" set to **No**
	* Settings: "Require that this column contains information" set to **Yes**
* **Owner**
	* Type: *Person* with "Allow multiple selections" set to **No**
	* Settings: "Require that this column contains information" set to **Yes**


## Minimal Path to Awesome

1. Download the solution file [TeamsAdaptiveCardRemindersFromLists.zip](/teams-adaptive-card-reminders-from-lists/solution/TeamsAdaptiveCardRemindersFromLists.zip)

 2. Import the solution using Power Automate. Click **My flows** and then click **Import** 

 	![Flow import](/samples/teams-adaptive-card-reminders-from-lists/assets/flow-import.png "Flow import")

3. Upload the solution by clicking **Upload** and select downloaded file from step 1

4. Configure the Flow connections by clicking on **Configuration** for both the *SharePoint Connection* and the *Microsoft Teams Connection*

 	![Import configuration before image](/samples/teams-adaptive-card-reminders-from-lists/assets/import-configuration-before.png "Import configuration before image")

5. For the **SharePoint Connection** either select an existing connection and click **Save** or add a new *SharePoint Connection* by clicking **Create new** (see Steps 5a, 5b)

	![Existing or new connection](/samples/teams-adaptive-card-reminders-from-lists/assets/existing-new-connection.png "Existing or new connection")

	5a. Click **Create a connection**, click **SharePoint** and then click **Create**

	![New SharePoint connection](/samples/teams-adaptive-card-reminders-from-lists/assets/sharepoint-connection.png "New SharePoint connection")

	5b. Select your account in the *Pick your account screen*

	5c. Return to the *Import package* screen, select your newly created *SharePoint Connection* and click **Save**

	![New SharePoint connection](/samples/teams-adaptive-card-reminders-from-lists/assets/save-sharepoint-connection.png "New SharePoint connection")

6. For the **Microsoft Teams Connection** either select an existing connection and click **Save** or add a new *Microsoft Teams Connection* by clicking **Create new** (see Steps 6a, 6b)

	![Existing or new connection](/samples/teams-adaptive-card-reminders-from-lists/assets/existing-new-connection.png "Existing or new connection")

	6a. Click **New connection**, select **Microsoft Teams** and then click **Create**

	6b. Select your account in the *Pick your account screen*

	6c. Return to the *Import package* screen, select your newly created *Microsoft Teams Connection* and click **Save**

	![New Teams connection](/samples/teams-adaptive-card-reminders-from-lists/assets/save-teams-connection.png "New Teams connection")

7. After our Flow connections have been created click **Import** to import the solution file.

	![Import configuration after image](/samples/teams-adaptive-card-reminders-from-lists/assets/import-configuration-after.png "Import configuration after image")

8. Click **Open flows** to further configure the flow

	![Open flow](/samples/teams-adaptive-card-reminders-from-lists/assets/open-flow.png "Open flow")

9. Expand *Initialize variable - varReminderDays*; this variable controls the number of days to notify in advance of the due date and can be changed as desired

	![varReminderDays](/samples/teams-adaptive-card-reminders-from-lists/assets/varReminderDays.png "varReminderDays")

10. Expand *Get items - Target list*, change the *Site address* and *List name* to your desired site and list

	![SharePoint Get items action](/samples/teams-adaptive-card-reminders-from-lists/assets/get-items.png "SharePoint Get items action")

11. Click **Save** to save your changes

	![Save and test](/samples/teams-adaptive-card-reminders-from-lists/assets/save-test.png "Save and test")

12. Click **Go back to previous page**

	![Previous page](/samples/teams-adaptive-card-reminders-from-lists/assets/previous-page.png "Previous page")

13. Click **Turn on** to enable your Flow

	![Turn on Flow](/samples/teams-adaptive-card-reminders-from-lists/assets/turn-on.png "Turn on Flow")

14. Click **Run** and then click **Run flow** to test your Flow; any list item with a due date on todays date plus the *varReminderDays* interval will trigger a *Microsoft Teams* adaptive card reminder message

	![Run Flow](/samples/teams-adaptive-card-reminders-from-lists/assets/run-flow.png "Run Flow")


Our adaptive card reminder looks like the image below. Clicking on the **More Info** button will take you to the list item. 

![Teams reminder message](/samples/teams-adaptive-card-reminders-from-lists/assets/teams-reminder.png "Teams reminder message")

The adaptive card was created and can be customized using the https://adaptivecards.io/designer/ site.


## Disclaimer

**THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**

## Help

> Note: don't worry about this section, we'll update the links.

We do not support samples, but we this community is always willing to help, and we want to improve these samples. We use GitHub to track issues, which makes it easy for  community members to volunteer their time and help resolve issues.

If you encounter any issues while using this sample, [create a new issue](https://github.com/pnp/powerautomate-samples/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&template=bug-report.yml&sample=YOURSAMPLENAME&authors=@YOURGITHUBUSERNAME&title=YOURSAMPLENAME%20-%20).

For questions regarding this sample, [create a new question](https://github.com/pnp/powerautomate-samples/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&template=question.yml&sample=YOURSAMPLENAME&authors=@YOURGITHUBUSERNAME&title=YOURSAMPLENAME%20-%20).

Finally, if you have an idea for improvement, [make a suggestion](https://github.com/pnp/powerautomate-samples/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&template=suggestion.yml&sample=YOURSAMPLENAME&authors=@YOURGITHUBUSERNAME&title=YOURSAMPLENAME%20-%20).

## For more information

- [Create your first flow](https://docs.microsoft.com/en-us/power-automate/getting-started#create-your-first-flow)
- [Microsoft Power Automate documentation](https://docs.microsoft.com/en-us/power-automate/)


<img src="https://telemetry.sharepointpnp.com/powerautomate-samples/samples/readme-template" />

---

