# Hide folders in a SharePoint Document library view

## Summary

SharePoint Online document library views can be shown with folders or as a flat structure, the show all items without folders option. This sample will demonstrate how you can update an existing view with this setting via Power Automate flow.

![picture of the sample](assets/preview.png)

![picture of the sample](assets/preview02.gif)

## Applies to

* [Microsoft Power Automate](https://docs.microsoft.com/power-automate/)

## Compatibility

![Premium License](https://img.shields.io/badge/Premium%20License-Not%20Required-green.svg "Premium license not required")
![On-Premises Connectors](https://img.shields.io/badge/On--Premises%20Connectors-No-green.svg "Does not use on-premise connectors")
![Custom Connectors](https://img.shields.io/badge/Custom%20Connectors-Not%20Required-green.svg "Does not use custom connectors")

## Authors

Solution|Author(s)
--------|---------
sharepoint-hide-folders-in-library-view | [Dennis Goedegebuure](https://github.com/expiscornovus) ([@expiscornovus](https://twitter.com/expiscornovus))

## Version history

Version|Date|Comments
-------|----|--------
1.0|November 18, 2022|Initial release

## Features

> Description of the sample with possible additional details than in short summary.

This sample illustrates the following concepts:

* Retrieve existing view by name
* Update view settings

## Minimal Path to Awesome

* [Download](./solution/sharepoint-hide-folders-in-library-view.zip) the `.zip` from the `solution` folder
* Within **Power Automate Studio**, import the solution .zip file using **Solutions** > **Import Solution** and select the .zip file you just downloaded.

## Using the Source Code

You can also use the [Power Apps CLI](https://docs.microsoft.com/powerapps/developer/data-platform/powerapps-cli) to pack the source code by following these steps::

* Clone the repository to a local drive
* Pack the source files back into a solution `.zip` file:
  ```bash
  pac solution pack --zipfile pathtodestinationfile --folder pathtosourcefolder --processCanvasApps
  ```
  Making sure to replace `pathtosourcefolder` to point to the path to this sample's `sourcecode` folder, and `pathtodestinationfile` to point to the path of this solution's `.zip` file (located under the `solution` folder)
* Within **Power Automate Studio**, import the solution `.zip` file using **Solutions** > **Import Solution** and select the `.zip` file you just packed.

## Disclaimer

**THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**

## Help

We do not support samples, but we this community is always willing to help, and we want to improve these samples. We use GitHub to track issues, which makes it easy for  community members to volunteer their time and help resolve issues.

If you encounter any issues while using this sample, [create a new issue](https://github.com/pnp/powerautomate-samples/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&template=bug-report.yml&sample=YOURSAMPLENAME&authors=@expiscornovus&title=sharepoint-hide-folders-in-library-view%20-%20).

For questions regarding this sample, [create a new question](https://github.com/pnp/powerautomate-samples/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&template=question.yml&sample=sharepoint-hide-folders-in-library-view&authors=@expiscornovus&title=sharepoint-hide-folders-in-library-view%20-%20).

Finally, if you have an idea for improvement, [make a suggestion](https://github.com/pnp/powerautomate-samples/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&template=suggestion.yml&sample=sharepoint-hide-folders-in-library-view&authors=@expiscornovus&title=sharepoint-hide-folders-in-library-view%20-%20).

## For more information

- [Create your first flow](https://docs.microsoft.com/en-us/power-automate/getting-started#create-your-first-flow)
- [Microsoft Power Automate documentation](https://docs.microsoft.com/en-us/power-automate/)


<img src="https://telemetry.sharepointpnp.com/powerautomate-samples/samples/readme-template" />

---
> Note that better pictures and documentation will increase the sample usage and the value you are providing for others. Thanks for your submissions in advance! You rock ❤.
> DELETE THIS PARAGRAPH BEFORE SUBMITTING