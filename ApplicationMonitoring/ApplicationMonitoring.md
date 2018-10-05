#  Application Monitoring
This is not a step-by-step guide. Instead it's a collection of screenshots which will help you complete the DevOpsHack challenges.
This is on purpose: We want you to explore and play with the different options of Azure DevOps.

## Use Analytics in ApplicationInsights in the Azure Portal

![Use Analytics in ApplicationInsights in the Azure Portal](/ApplicationMonitoring/LogAnalytics.png)

https://docs.microsoft.com/en-us/azure/log-analytics/query-language/get-started-analytics-portal?toc=/azure/azure-monitor/toc.json


## Collect telemetry about search times
In the file /Controllers/SearchController.cs in method Index() provide these lines of code:

```
// add ApplicationInsights namespace
using Microsoft.ApplicationInsights;

// create an instance of the telemetry client in class scope
public class SearchController : Controller
{
...
    private TelemetryClient _telemetry = new TelemetryClient();
...
}

// Start timer
var now = DateTime.Now;

var result = await _search.Search(q);

// stop passed time
var passed = DateTime.Now;

// add properties
var props = new Dictionary<string, string>
{
    { "QueryName", "Search" },
    { "QueryString", q}
};

// add measurments
var measurements = new Dictionary<string, double>
{
    {"TimeInMilliseconds", passed.Subtract(now).TotalMilliseconds }
};

// track event
_telemetry.TrackEvent("SqlDatabase", props, measurements);

```

## Create an availability test in the portal
In the portal look for the AI component for your Dev environment and add an availabiltiy test. Explore the settings!
![Add availability test](/ApplicationMonitoring/images/ApplicationMonitoringAvailabilityTest.jpg)

## Create a Work Item in the portal
Starting in your application insights view in Azure Portal go and follow down the Page View metric until you find the requests. Choose one and look for the "New Work Item" button. Configure it for your account for first time usage.
![Create a Work Item in Azure Portal ](/ApplicationMonitoring/images/ApplicationMonitoringNewWorkItem.jpg)

## Modify your Azure DevOps Dashboard
Right click the icon in the lower right corner to start modifying your dashboard. Add the Azure Application Insights Widget. If not available get it from the marketplace. To find out how to modify it, follow the "Learn more" link.

![Modify dashboard ](/ApplicationMonitoring/images/ApplicationMonitoringDashboardMod.jpg)