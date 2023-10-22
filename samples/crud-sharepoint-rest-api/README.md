# Get SharePoint Site Information

## Summary

This sample solution covers CRUD operations when using SharePoint REST API inside Power Automate.

## Flows

* create-item-in-another-list (available)
* update-item-in-another-list (coming soon)

#### create-item-in-another-list
This flow illustrates the process of creating a new list item in a secondary list (Target List) from a source list (CreateList) using the 'Send an HTTP request to SharePoint' action in Power Automate. It covers commonly used fields including: Content Type, Date, Date and Time, Hyperlink, Multi-select Choice, Multi-select People Picker, Number, Single Choice, Single Line of Text, Single People Picker, and Yes/No. Additionally, this flow can handle null values from these fields efficiently.

This sample workflow is intended to serve as a valuable reference for interacting with the SharePoint REST API within Power Automate.

![preview01](assets/preview01.png)

***update-item-in-another-list (coming soon)***

## Applies to

* [Microsoft Power Automate](https://docs.microsoft.com/power-automate/)

## Compatibility

![Premium License](https://img.shields.io/badge/Premium%20License-Not%20Required-green.svg "Premium license not required")
![On-Premises Connectors](https://img.shields.io/badge/On--Premises%20Connectors-No-green.svg "Does not use on-premise connectors")
![Custom Connectors](https://img.shields.io/badge/Custom%20Connectors-Not%20Required-green.svg "Does not use custom connectors")

## Authors

Solution|Author(s)
--------|---------
crud-sharepoint-rest-api | [Gabriel Koolman](https://www.linkedin.com/in/gabrielkoolman/)

## Version history

Version|Date|Comments
-------|----|--------
1.0|October 22, 2023|Initial release

## Minimal Path to Awesome

* Create a new SharePoint list and name it "CreateList"
* Add the required columns (you can find the column names and types [here](assets/sp-column-config.json))
* Using "CreateList" as a template, create a new SharePoint list and name it "TargetList"
* [Download](solution/crud-sharepoint-rest-api.zip) the `.zip` file from the `solution` folder
* Import the solution by going to the [Power Automate Portal](https://make.powerautomate.com) and clicking on **"Import Solution"**
* Configure the (4) environment variables
* Turn on the flow

## Using the Source Code

You can also use the [Power Platform CLI](https://docs.microsoft.com/powerapps/developer/data-platform/powerapps-cli) to pack the source code by following these steps::

* Clone the repository to a local drive
* Pack the source files back into a solution `.zip` file:
  ```bash
  pac solution pack --zipfile pathtodestinationfile --folder pathtosourcefolder
  ```
  Making sure to replace `pathtosourcefolder` to point to the path to this sample's `sourcecode` folder, and `pathtodestinationfile` to point to the path of this solution's `.zip` file (located under the `solution` folder)
* Import the solution by going to the [Power Automate Portal](https://make.powerautomate.com) and clicking on **"Import Solution"**

## Disclaimer

**THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**

## Help

If you encounter any issues while using this sample, [create a new issue](https://github.com/pnp/powerautomate-samples/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&template=bug-report.yml&sample=YOURSAMPLENAME&authors=@YOURGITHUBUSERNAME&title=YOURSAMPLENAME%20-%20).

For questions regarding this sample, [create a new question](https://github.com/pnp/powerautomate-samples/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&template=question.yml&sample=YOURSAMPLENAME&authors=@YOURGITHUBUSERNAME&title=YOURSAMPLENAME%20-%20).

Finally, if you have an idea for improvement, [make a suggestion](https://github.com/pnp/powerautomate-samples/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&template=suggestion.yml&sample=YOURSAMPLENAME&authors=@YOURGITHUBUSERNAME&title=YOURSAMPLENAME%20-%20).

## For more information

- [Create your first flow](https://docs.microsoft.com/en-us/power-automate/getting-started#create-your-first-flow)
- [Microsoft Power Automate documentation](https://docs.microsoft.com/en-us/power-automate/)

<img src="https://telemetry.sharepointpnp.com/powerautomate-samples/samples/readme-template" />
