# Security and data collection

ThoughtFarmer Intranet Statistics is a client side scripting package. So all data is sent from your users' browsers directly to our statistics servers. This page goes over some of the security and data collection details for the gathering and transfer of statistics information.

### Data security <a id="section2"></a>

All data is sent to Intranet Statistics using SSL. Only a limited number of ThoughtFarmer staff have access to the Intranet Statistics server. The server is set up as a "multi-tenant" approach, with data for multiple companies stored in the same database. All data is backed up on a nightly basis.

### List of fields sent to Intranet Statistics <a id="section3"></a>

* **action\_name**: The title of the action being tracked. 
* **idsite**: The ID of the website it was tracked for
* **rec**: Required for tracking, must be set to one, eg, &rec=1.
* **r**: Meant to hold a random value that is generated before each request. Using it helps avoid the tracking request being cached by the browser or a proxy.
* **h**: The current hour \(local time\).
* **m**: The current minute \(local time\).
* **s**: The current second \(local time\).
* **url**: The full URL for the current action.
* **urlref**: The full HTTP Referrer URL
* **\_id**: The unique visitor ID, must be a 16 characters hexadecimal string. If this value is not set Intranet Statistics will still track visits, but the unique visitors metric might be less accurate.
* **\_idts**: The UNIX timestamp of this visitor's first visit. 
* **\_idvc**: The current count of visits for this visitor. 
* **\_viewts**: The UNIX timestamp of this visitor's previous visit. 
* **pdf**: Plugins used by the visitor can be specified by setting the following parameters to 1 - Adobe Acrobat.
* **qt**: Plugins used by the visitor can be specified by setting the following parameters to 1 - Quicktime.
* **realp**: Plugins used by the visitor can be specified by setting the following parameters to 1 - realplayer.
* **wma**: Plugins used by the visitor can be specified by setting the following parameters to 1 - Windows Media.
* **dir**: Plugins used by the visitor can be specified by setting the following parameters to 1 - Director.
* **fla**: Plugins used by the visitor can be specified by setting the following parameters to 1 - Flash.
* **java**: Plugins used by the visitor can be specified by setting the following parameters to 1 - Java.
* **gears**: Plugins used by the visitor can be specified by setting the following parameters to 1 - Gears.
* **ag**: Plugins used by the visitor can be specified by setting the following parameters to 1 - Silverlight.
* **cookie**: When set to 1, the visitor's client is known to support cookies.
* **res**: The resolution of the device the visitor is using, eg 1280x1024.
* **dimension1**: user full name
* **dimension2**: Thoughfarmer page hiearchy tree \(e.g. Home &gt; Page &gt; Sub page \)
* **dimension3**: event action \(page create, page edit, page comment, search\)
* **gt\_ms**: The amount of time it took the server to generate this action, in milliseconds. This value is used to process the Page speed report Avg. generation time column in the Page URL and Page Title reports, as well as a site wide running average of the speed of your server.

  **Data retention**

  Raw tracking data is retained for 60 days. Aggregated figures will be stored indefinitely.

  **Frequency of report aggregation**

  * Daily reports are calculated every 15 minutes.
  * Weekly, monthly and yearly reports are calculated every 6 hours.
  * Date Range reports are calculated in real time the first time you select a date range, and then cached for 2 hours.

  **Patriot Act**

  Data is hosted at the Vancouver data center of Gossamer Threads. Gossamer is a Canadian owned company with no operations in the USA, so your data will not be subject to the US Patriot Act.

  **On-premise installations**

  If you would like to run your own installation of Intranet Statistics locally, the installation package and instructions can be found on the [Self-Hosted Intranet Statistics](../thoughtfarmer-analytics/self-hosted-intranet-statistics.md) page.

  Support for a local instance of Intranet Statistics is not included in a standard support contract, but can be supported under a Platinum Support contract.

  **Known issues**

  * Choosing long date ranges may cause out-of-memory errors if you have a busy site.
  * IE 8 and 9 users show up as IE 7 in Intranet Statistics.

