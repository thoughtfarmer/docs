# External RSS feed status

### How to use the External RSS feed status page

The External RSS feed status page allows you to monitor the status of external RSS feeds that are feeding information to your intranet. It lists all of the external RSS feeds that have been added to pages on your intranet, and alerts you to feeds that are not working correctly.

![](../../.gitbook/assets/1%20%2877%29.jpg)

External RSS feeds are listed in two sections: **Valid feeds** and **Invalid feeds**. Valid feeds are feeds that are successfully transmitting information to the intranet. Invalid feeds are feeds that the intranet has encountered errors in connecting to. You can see when a feed last synced successfully, or when it encountered its last connection error.  
  
RSS feeds may go offline when the feed URL changes, or for other reasons. When a feed goes offline, the intranet cannot connect to it, and error messages will be generated in the [system logs](../behind-the-scenes/system-logs.md) every 30 minutes \(or the time period specified for the configuration setting feeds.external.polling.period\) when the service tries to get data from the feed.  
  
This page indicates how many pages are using each RSS feed. Click on the number of pages beside the Feed title and URL to see a modal with the titles and breadcrumbs of the pages displaying that feed.  


![](../../.gitbook/assets/2%20%2876%29.jpg)

Click on the RSS Feed title to go to the Feed page where you can edit or delete the Feed. Click on View response ****on the right to see the raw feed.  
  
To learn more about editing RSS Feeds, see the page [RSS Feeds](../customize-your-content/rss-feeds.md).

