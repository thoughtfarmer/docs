# Set up a campaign

Campaigns in Intranet Statistics provide you with a way to monitor the referrers to ThoughtFarmer. This way you can track how successful a particular campaign was. Optionally, you can specify keywords for a single campaign in order to track the method by which they were reached. For example, you could create a launch campaign and specify the method of entry using keywords such as "email", "homepage, or "external". Campaigns can then be matched with specific goals and conversions to see how well a campaign is doing in producing a desired action by your users.

####  Create a campaign

Campaign tracking in Piwik is all done via specific URL parameters. So if a link to the intranet, or a specific page on the intranet contains these URL parameters then Piwik will track that as campaign data. So there is no direct campaign creation interface in Piwik. Instead, you construct the URLs as desired, then distribute in your campaign media accordingly.  
  
The following example is a campaign called Get-Started. The link is designed to go to a specific page on the intranet. We wish to specify whether users are accessing the page via an email sent, or a banner ad on the homepage. To do this we create a campaign, and keyword URLs:

* **Link to page**: http://intranet/content/1234
* **Link to page with campaign**: http://intranet/content/1234?pk\_campaign=Get-Started
* **Link to page with campaign and keyword \(email\):** http://intranet/content/1234?pk\_campaign=Get-Started&pk\_kwd=email
* **Link to page with campaign and keyword \(homepage\):** http://intranet/content/1234?pk\_campaign=Get-Started&pk\_kwd=homepage

  
The easiest method to create these URLs is to go to the **Referrers** &gt; **Campaigns** section of Piwik and click the **URL Builder tool** link. Or you can access directly from here at [http://piwik.org/docs/tracking-campaigns/url-builder/](http://piwik.org/docs/tracking-campaigns/url-builder/). You can then take the generated URLs and add them to the proper place. For links in ThoughtFarmer you can use the regular Link browser. However, insert the above URL as an "External" link even though technically it is an internal ThoughtFarmer link.  
  
Data for that campaign will begin to be tracked as soon as users start using those links.  
 

#### Viewing campaign data

If you just launched a campaign and want to see live stats of the usage you can see this in the homepage widget "Visitors in Real Time". Any campaign data will display here as shown in the example below:  
  
![real+time+campaign.png](https://community.thoughtfarmer.com/imagethumb/19768270000/17274/300x71/False/real+time+campaign.png)  
  
To view campaign data reports go to the **Referrers** &gt; **Campaigns** section in Piwik. Select the desired date range keeping in mind the [report generation times](https://community.thoughtfarmer.com/content/105880). The report is available in the following data views:  
  
**Default view \(click the campaign name to drill into keywords\):**  
![campaign+default.png](https://community.thoughtfarmer.com/imagethumb/22809530000/17275/406x266/False/campaign+default.png)  
  
**Enhanced view \(by clicking the** ![enhanced+icon.png](https://community.thoughtfarmer.com/imagethumb/23885000000/17276/1000x1000/False/enhanced+icon.png) **icon\):**  
![campaign+enhanced+view.png](https://community.thoughtfarmer.com/imagethumb/26709230000/17279/449x219/False/campaign+enhanced+view.png)  
  
  
**Goal metrics view \(by clicking the** ![conversion+icon.png](https://community.thoughtfarmer.com/imagethumb/25105770000/17277/1000x1000/False/conversion+icon.png) **icon\):**  
![Campaign+-+goal+metrics+view.png](https://community.thoughtfarmer.com/imagethumb/26229230000/17278/559x274/False/Campaign+-+goal+metrics+view.png)  
  
  
You can also use the bar graph, pie chart, or tag cloud views if desired.  


