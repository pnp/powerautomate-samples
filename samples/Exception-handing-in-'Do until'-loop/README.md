# Pattern: Exception handing in 'Do until'-loop
## Summary

A pattern for breaking out of a 'Do Until'-loop in Power Automate when an exception occurs.

![picture of the flow](assets/flow.png)

## Applies to

* [Microsoft Power Automate](https://docs.microsoft.com/en-us/power-automate/getting-started)
* [Azure Logic Apps](https://docs.microsoft.com/en-us/azure/logic-apps/logic-apps-overview)

## Solution

Solution|Author(s)
--------|---------
PatternExceptionhandingin'Dountil'-loop | [Remy Blok](https://github.com/remyblok), Prodware

## Version history

Version|Date|Comments
-------|----|--------
1.0|May 01, 2021|Initial release

## Disclaimer

**THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**

---

## Minimal Path to Awesome

* [Download](solution\PatternExceptionhandingin'Dountil'-loop.zip) the `.zip` from the `solution` folder
* [Import](https://flow.microsoft.com/en-us/blog/import-export-bap-packages/) the `.zip` file using **My Flows** > **Import** > **Upload** within Microsoft Flow.

## Features

Power Automate has the ['Do Until' action](https://docs.microsoft.com/en-us/azure/logic-apps/logic-apps-control-flow-loops#until-loop), which allows the actions within to be repeated until a condition is met. You can configure how often and how long this is repeated. This way you can create long running processes (up to 30 days). By default, if an error occurs in the loop then it just continues with the next cycle in the loop. 

If an unexpected error, i.e. an exception, would occur in a long running loop, it is not easily visible in Power Automate. Only after the run has fully finished you see the results. So, most of the time it is preferred to stop the loop if an exception has occured. 

In this sample we use a Scope inside the 'Do Until'-loop. Now, a Scope does fail immediately if one of the child actions fail. By setting the 'Configure run after' to run only on error of the Scope we can set a variable only if an error has occured.
![Go to Run After](assets/runAfter.png) 
![Go to Run After](assets/runAfterSettings.png)

Just as in de documentation we use a variable in the condition of the loop to check if the loop should continue. This variable is also used afte the loop to determine if the loop has been succesful or resulted in an exception. In this sample it is used to terminate the Flow with the correct status. This makes it easy to see if a Flow run has failed or not. 

Note: there is a clear distinctin between an expected and unexpected error. For example, if you call a webservice and it is documented a HTTP 404 status is returned, then Power Automate will see this as an error, but we can expect this to happen and should handle this gracefully. On the other hand, if a HTTP 500 error occurs then this is unexpected and an exception, the flow should now probably fail so you can investiage whats wrong as soon as possible.

Note 2: Make sure that you setup the correct retry policies on the individual actions. This makes sure that intermittened failures caused by, for example, network issues or a server with a hickup do not result in errors in your Flow. See [Retry policy in Logic Apps](https://docs.microsoft.com/en-us/azure/logic-apps/logic-apps-exception-handling) for more information.

<img src="https://telemetry.sharepointpnp.com/powerfx-samples/samples/readme-template" />
