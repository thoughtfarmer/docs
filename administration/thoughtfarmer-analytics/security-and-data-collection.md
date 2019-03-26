# Security and data collection



ThoughtFarmer sends data to the ThoughtFarmer Analytics server using client side scripting. So all data is sent directly from your users' browsers to our analytics servers. This page describes some details of security and data collection for the gathering and transfer of statistics information.

### Data security <a id="section2"></a>

All data is sent to ThoughtFarmer Analytics using SSL. Only a limited number of ThoughtFarmer staff have access to the ThoughtFarmer Analytics server. The server is set up as a "multi-tenant" approach, with data for multiple companies stored in the same database. All data is backed up on a nightly basis.

### List of actual fields sent to ThoughtFarmer Analytics <a id="section3"></a>

* **action\_name**: The title of the action being tracked. 
* **idsite**: The ID of the website it was tracked for.
* **rec**: Required for tracking, must be set to one, eg, &rec=1.
* **r**: Meant to hold a random value that is generated before each request. Using it helps avoid the tracking request being cached by the browser or a proxy.
* **h**: The current hour \(local time\).
* **m**: The current minute \(local time\).
* **s**: The current second \(local time\).
* **url**: The full URL for the current action.
* **urlref**: The full HTTP Referrer URL
* **\_id**: The unique visitor ID, must be a 16 character hexadecimal string. If this value is not set ThoughtFarmer Analytics will still track visits, but the unique visitors metric might be less accurate.
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
* **dimension\_1**: Currently, this field is used for sending ThoughtFarmer user full name.
* **dimension\_2**: Currently, this field is user for sending ThoughtFarmer page tree path.
* **dimension\_3**: Currently, this field is used for sending ThoughtFarmer action type name \(e.g. 'create', 'edit', 'comment', 'search'\).
* **gt\_ms**: The amount of time it took the server to generate this action, in milliseconds. This value is used to process the Avg. Generation Time column in the Page URL and Page Title reports, as well as a site-wide running average of the speed of your server.

### Data retention <a id="section4"></a>

Raw tracking data is retained for 60 days. Aggregated figures will be stored indefinitely.

### Frequency of report aggregation <a id="section5"></a>

* Daily reports are calculated every 15 minutes.
* Weekly, monthly and yearly reports are calculated every 6 hours.
* Date Range reports are calculated in real time the first time you select a date range, and then cached for 2 hours.

### Patriot Act <a id="section6"></a>

Data is hosted at the Vancouver data center of Gossamer Threads. Gossamer is a Canadian-owned company with no operations in the USA, so your data will not be subject to the US Patriot Act.

### Known issues <a id="section8"></a>

* Choosing long date ranges may cause out-of-memory errors if you have busy site traffic.

