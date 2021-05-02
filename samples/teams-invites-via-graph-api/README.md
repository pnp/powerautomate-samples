# Teams Guest Access with Approval

## Summary

This sample project allows a guest user to request access to a Team. The owner(s) of the Team will first Approve the request before the guest account is added to the Tenant along with access to the team

## Applies to

*   [Micorosoft Power Automate](https://docs.microsoft.com/power-automate/)

## Compatibility

![Premium License](https://img.shields.io/badge/Premium%20Power%20Automate-Required-orange)

  
 

![On-Premises Connectors](https://img.shields.io/badge/On--Premises%20Connectors-No-green.svg)

  
 

![Custom Connectors](https://img.shields.io/badge/Custom%20Connectors-%20Required-orange.svg)

## Authors

| Solution | Author(s) |
| --- | --- |
| Teams-Invites-Via-Graph-API | [Carl Cookson](https://github.com/LinkeD365) ([@LinkeD365](https://twitter.com/LinkeD365)) |

## Version history

| Version | Date | Comments |
| --- | --- | --- |
| 1.0 | May 1st, 2021 | Initial release |

## Features

This sample demonstrates the following concepts:

*   Use of Microsoft Forms input to trigger Power Automate
*   Development of a Custom Connector to connect to Microsoft Graph API
*   Use of standard Power Automate Approvals
*   Adding Guest users to Tenant via Custom Connector/Graph API
*   Adding user to Team

## Disclaimer

**THIS CODE IS PROVIDED** _**AS IS**_ **WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**

## Minimal Path to Awesome

As we are using the Graph API, you need to allow your Power Automate to access it. This is done in Azure Active Directory and you need the appropriate rights on your tenant to do this. It is an administrative function, so check with your Azure Administrator.

1.  Connect to [https://aad.portal.azure.com/](https://aad.portal.azure.com/) and sign in with an appropriate administrator account.
2.  Select Azure Active Directory/App Registrations
3.  Select New Registration, enter a name and press Register.
4.  Take Note of the Application (client) ID value, marked in yellow in screenshot below

*   [Download](https://github.com/pnp/powerautomate-samples/blob/main/samples/teams-invites-via-graph-api/customconnector/GraphAPI.swagger.json) the '.json' file from the customconnector folder.
*   Use the JSON file to create a new custom connector via
