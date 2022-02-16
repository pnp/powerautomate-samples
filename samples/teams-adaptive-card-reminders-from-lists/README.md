# Teams Adaptive Card Reminders From Lists

## Summary

This sample will send a *Microsoft Teams* adaptive card reminder from *Microsoft Lists* to the item owner in advance of the due date using *Power Automate*.

[![Flow overview](/teams-adaptive-card-reminders-from-lists/assets/flow-overview.png "Flow overview")](/teams-adaptive-card-reminders-from-lists/assets/flow-overview.png "Flow overview")

## Requirements
This Flow requires the following Microsoft List columns and settings:
* **Title**
	* Settings: "Require that this column contains information" set to **Yes**
* **DueDate**
	* Type: Date time with "Include time" set to **No**
	* Settings: "Require that this column contains information" set to **Yes**
* **Owner**
	* Type: Person with "Allow multiple selections" set to **No**
	* Settings: "Require that this column contains information" set to **Yes**

## Import Solution

 1. Download the solution file [TeamsAdaptiveCardRemindersFromLists.zip](/teams-adaptive-card-reminders-from-lists/solution/TeamsAdaptiveCardRemindersFromLists.zip)

 2. Import the solution using Power Automate. Click **My flows** and then click **Import** 

 	[![Flow import](/teams-adaptive-card-reminders-from-lists/assets/flow-import.png "Flow import")](/teams-adaptive-card-reminders-from-lists/assets/flow-import.png "Flow import")

3. Upload the solution by clicking **Upload** and select downloaded file from step 1

4. Configure the Flow connections by clicking on **Configuration** for both the *SharePoint Connection* and the *Microsoft Teams Connection*

 	[![Import configuration before image](/teams-adaptive-card-reminders-from-lists/assets/import-configuration-before.png "Import configuration before image")](/teams-adaptive-card-reminders-from-lists/assets/sharepoint-connection.png "Import configuration before image")

5. For the **SharePoint Connection** either select an existing connection and click **Save** or add a new *SharePoint Connection* by clicking **Create new** (see Steps 5a, 5b)

	[![Existing or new connection](/teams-adaptive-card-reminders-from-lists/assets/existing-new-connection.png "Existing or new connection")](/teams-adaptive-card-reminders-from-lists/assets/existing-new-connection.png "Existing or new connection")

	5a. Click **Create a connection**, click **SharePoint** and then click **Create**

	[![New SharePoint connection](/teams-adaptive-card-reminders-from-lists/assets/sharepoint-connection.png "New SharePoint connection")](/teams-adaptive-card-reminders-from-lists/assets/import-configuration-before.png "New SharePoint connection")

	5b. Select your account in the *Pick your account screen*

	5c. Return to the *Import package* screen, select your newly created *SharePoint Connection* and click **Save**

	[![New SharePoint connection](/teams-adaptive-card-reminders-from-lists/assets/save-sharepoint-connection.png "New SharePoint connection")](/teams-adaptive-card-reminders-from-lists/assets/save-sharepoint-connection.png "New SharePoint connection")

6. For the **Microsoft Teams Connection** either select an existing connection and click **Save** or add a new *Microsoft Teams Connection* by clicking **Create new** (see Steps 6a, 6b)

	[![Existing or new connection](/teams-adaptive-card-reminders-from-lists/assets/existing-new-connection.png "Existing or new connection")](/teams-adaptive-card-reminders-from-lists/assets/existing-new-connection.png "Existing or new connection")

	6a. Click **New connection**, select **Microsoft Teams** and then click **Create**

	6b. Select your account in the *Pick your account screen*

	6c. Return to the *Import package* screen, select your newly created *Microsoft Teams Connection* and click **Save**

	[![New Teams connection](/teams-adaptive-card-reminders-from-lists/assets/save-teams-connection.png "New Teams connection")](/teams-adaptive-card-reminders-from-lists/assets/save-teams-connection.png "New Teams connection")

7. After our Flow connections have been created click **Import** to import the solution file.

	[![Import configuration after image](/teams-adaptive-card-reminders-from-lists/assets/import-configuration-after.png "Import configuration after image")](/teams-adaptive-card-reminders-from-lists/assets/import-configuration-after.png "Import configuration after image")

8. Click **Open flows** to further configure the flow

	[![Open flow](/teams-adaptive-card-reminders-from-lists/assets/open-flow.png "Open flow")](/teams-adaptive-card-reminders-from-lists/assets/open-flow.png "Open flow")

9. Expand *Initialize variable - varReminderDays*; this variable controls the number of days to notify in advance of the due date and can be changed as desired

	[![varReminderDays](/teams-adaptive-card-reminders-from-lists/assets/varReminderDays.png "varReminderDays")](/teams-adaptive-card-reminders-from-lists/assets/varReminderDays.png "varReminderDays")

10. Expand *Get items - Target list*, change the *Site address* and *List name* to your desired site and list

	[![SharePoint Get items action](/teams-adaptive-card-reminders-from-lists/assets/get-items.png "SharePoint Get items action")](/teams-adaptive-card-reminders-from-lists/assets/get-items.png "SharePoint Get items action")

11. Click **Save** to save your changes

	[![Save and test](/teams-adaptive-card-reminders-from-lists/assets/save-test.png "Save and test")](/teams-adaptive-card-reminders-from-lists/assets/save-test.png "Save and test")

12. Click **Go back to previous page**

	[![Previous page](/teams-adaptive-card-reminders-from-lists/assets/previous-page.png "Previous page")](/teams-adaptive-card-reminders-from-lists/assets/previous-page.png "Previous page")

13. Click **Turn on** to enable your Flow

	[![Turn on Flow](/teams-adaptive-card-reminders-from-lists/assets/turn-on.png "Turn on Flow")](/teams-adaptive-card-reminders-from-lists/assets/turn-on.png "Turn on Flow")

14. Click **Run** and then click **Run flow**to test your Flow; any list item with a due date on todays date plus the *varReminderDays* interval will trigger a Microsoft Teams adaptive card reminder message

	[![Run Flow](/teams-adaptive-card-reminders-from-lists/assets/run-flow.png "Run Flow")](/teams-adaptive-card-reminders-from-lists/assets/run-flow.png "Run Flow")


Our reminder looks like the image below. Clicking on the **More Info** button will take you to the list item. 

[![Teams reminder message](/teams-adaptive-card-reminders-from-lists/assets/teams-reminder.png "Teams reminder message")](/teams-adaptive-card-reminders-from-lists/assets/teams-reminder.png "Teams reminder message")

The adaptive card was created and can be customized using the https://adaptivecards.io/designer/ site.