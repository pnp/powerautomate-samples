# Create folder with link back to list

## Summary

This sample creates a folder in a *SharePoint* document library and then stores the link to the newly created folder inside of *Microsoft Lists* using *Power Automate*. The folder name is based on a combination of list columns and provides a better link experience compared to the default URL. 

![Flow overview](/samples/create-folder-with-link-back-to-list/assets/flow-overview.png "Flow overview")


## Applies to

* [Power Automate](https://docs.microsoft.com/power-automate/)
* [SharePoint](https://learn.microsoft.com/en-us/sharepoint/)

## Compatibility

![Premium License](https://img.shields.io/badge/Premium%20License-Not%20Required-green.svg "Premium license not required")
![On-Premises Connectors](https://img.shields.io/badge/On--Premises%20Connectors-No-green.svg "Does not use on-premise connectors")
![Custom Connectors](https://img.shields.io/badge/Custom%20Connectors-Not%20Required-green.svg "Does not use custom connectors")


## Authors

Solution|Author(s)
--------|---------
create-folder-with-link-back-to-list | [Norm Young](https://github.com/nyoung30) ([@stormin_30](https://twitter.com/stormin_30))


## Version history

Version|Date|Comments
-------|----|--------
1.0|October 10, 2022|Initial release


## Features

This sample illustrates the following concepts:

* Expressions
* SharePoint REST API
* Variables


## Prerequisites

This Flow requires the following list columns and settings:
* **Title**
	* Settings: "Require that this column contains information" set to **Yes**
* **FolderLocation**
	* Type: *Hyperlink* 


## Minimal Path to Awesome

1. Download the solution file [CreateFolderWithLinkBackToList.zip](/samples/create-folder-with-link-back-to-list/solution/CreateFolderWithLinkBackToList.zip)

2. Import the solution using *Power Automate*. Click **My flows**, click **Import** and then click **Import Package (Legacy)**

 	![Flow import](/samples/create-folder-with-link-back-to-list/assets/flow-import.png "Flow import")

3. Upload the solution by clicking **Upload** and select the downloaded file from Step 1

	![Upload package](/samples/create-folder-with-link-back-to-list/assets/upload-package.png "Upload package")

4. Configure the *Flow* connections by clicking on **Configuration** for the *SharePoint Connection*

 	![Import configuration before image](/samples/create-folder-with-link-back-to-list/assets/import-configuration-before.png "Import configuration before image")

5. Select an existing connection and click **Save** or add a new *SharePoint Connection* by clicking **Create new** (see Steps 5a, 5b)

	![Existing or new connection](/samples/create-folder-with-link-back-to-list/assets/existing-new-connection.png "Existing or new connection")

	5a. Click **Create a connection**, click **SharePoint** and then click **Create**

	![New SharePoint connection](/samples/create-folder-with-link-back-to-list/assets/sharepoint-connection.png "New SharePoint connection")

	5b. Select your account in the *Pick your account screen*

	5c. Return to the *Import setup* screen, select your newly created *SharePoint Connection* and click **Save**

	![New SharePoint connection](/samples/create-folder-with-link-back-to-list/assets/save-sharepoint-connection.png "New SharePoint connection")

6. After our Flow connections have been created click **Import** to import the solution file.

	![Import configuration after](/samples/create-folder-with-link-back-to-list/assets/import-configuration-after.png "Import configuration after")

	**Note:** If you receive a "GetTable" error during the import, click the **Save as a new flow** option and manually update the connections references. This error is caused by importing and exporting *Flows* between tenants.

	![Flow import error](/samples/create-folder-with-link-back-to-list/assets/flow-import-error.png "Flow import error")
	
	Select your target connection to fix the "Invalid connection" error. Repeat for all SharePoint actions.
	![Fix connections](/samples/create-folder-with-link-back-to-list/assets/flow-fix-connections.png "Fix connections")

7. Click **Open flow** to further configure the flow

	![Open flow](/samples/create-folder-with-link-back-to-list/assets/open-flow.png "Open flow")
	
8. Expand the *When an item is created*, change the *Site address* and *List name* to your desired site and list 

	![Configure When an item is created](/samples/create-folder-with-link-back-to-list/assets/when-an-item-is-created.png "Configure When an item is created")

9.  Expand *Initialize variable - varParameters*, change the *Site address* and *List name* to your desired site and list

	![Configure Initialize variable](/samples/create-folder-with-link-back-to-list/assets/initialize-variable.png "Configure Initialize variable")

	Name | Value
	---- | ------
	*varSiteURL* | Replace with your site URL
	*varListInternalName* | Replace with your internal list name; **Tip:** Use this API call in your browser to obtain the internal list name: *https://YourTenantName.sharepoint.com/sites/YourSiteName/_api/Web/Lists/GetByTitle('<YourListNameWithSpaces')?$select=ListItemEntityTypeFullName*
	*varListDisplayName* | Replace with your list display name
	*varColumnInternalName* | Replace with the internal column name; **Tip:** Use the list column settings to see the internal name at the end of the URL string
	*varDocumentDisplayLibraryName* | Replace with the Document Library display name.
	*varFolderName* | Update the expression as required; by default the expression concatenates the list ID column with the Title column values: *concat(triggerOutputs()?['body/ID'], '-', triggerOutputs()?['body/Title'])*

10. Click **Save** to save your changes

	![Save](/samples/create-folder-with-link-back-to-list/assets/save.png "Save")

11. Click **Go back to previous page**

	![Previous page](/samples/create-folder-with-link-back-to-list/assets/previous-page.png "Previous page")

12. Click **Turn on** to enable your Flow

	![Turn on Flow](/samples/create-folder-with-link-back-to-list/assets/turn-on.png "Turn on Flow")

13. Test your *Flow* by adding a new item to your list. If successful the Flow will:
    1.  Create a folder in our target *SharePoint* Document Library with a name that concatenates the *ID* and *Title* columns
    2.  Update list item *FolderLocation* column to match the folder name
![Your flow ran successfully](/samples/create-folder-with-link-back-to-list/assets/flow-run.png "Your flow ran successfully")

Our list item looks like the image below. Clicking on the *FolderLocation* link will take you to the folder location. 

![List item](/samples/create-folder-with-link-back-to-list/assets/list-item.png "List item")

![Folder](/samples/create-folder-with-link-back-to-list/assets/folder.png "Folder")


## Disclaimer

**THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**

## Help

We do not support samples, but we this community is always willing to help, and we want to improve these samples. We use GitHub to track issues, which makes it easy for  community members to volunteer their time and help resolve issues.

If you encounter any issues while using this sample, [create a new issue](https://github.com/pnp/powerautomate-samples/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&template=bug-report.yml&sample=YOURSAMPLENAME&authors=@YOURGITHUBUSERNAME&title=YOURSAMPLENAME%20-%20).

For questions regarding this sample, [create a new question](https://github.com/pnp/powerautomate-samples/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&template=question.yml&sample=YOURSAMPLENAME&authors=@YOURGITHUBUSERNAME&title=YOURSAMPLENAME%20-%20).

Finally, if you have an idea for improvement, [make a suggestion](https://github.com/pnp/powerautomate-samples/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&template=suggestion.yml&sample=YOURSAMPLENAME&authors=@YOURGITHUBUSERNAME&title=YOURSAMPLENAME%20-%20).

## For more information

- [Create your first flow](https://docs.microsoft.com/en-us/power-automate/getting-started#create-your-first-flow)
- [Microsoft Power Automate documentation](https://docs.microsoft.com/en-us/power-automate/)


<img src="https://telemetry.sharepointpnp.com/powerautomate-samples/samples/readme-template" />

---