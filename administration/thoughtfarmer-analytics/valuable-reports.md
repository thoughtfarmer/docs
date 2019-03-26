# Valuable reports

ThoughtFarmer Analytics provides dozens of ready-to-go reports available as widgets and exportable into various formats. There is a wealth of valuable information available. As well, since ThoughtFarmer Analytics is using Matomo, a 3rd party open-source analytics package originally intended for anonymous sites with e-commerce capabilities, there are some reports that may be less valuable or irrelevant for your ThoughtFarmer site.  
  
This page serves to give an outline of some of the most valuable reports in ThoughtFarmer for intranet managers. It also includes some tips on how to get the most out of those reports.   
  
**On this page:**

* [Visitor Overview](../intranet-statistics/valuable-reports.md)
* [Visits Per Duration](../intranet-statistics/valuable-reports.md)
* [Visits Real-time](../intranet-statistics/valuable-reports.md)
* [Users](../intranet-statistics/valuable-reports.md)
* [Search keywords](../intranet-statistics/valuable-reports.md)
* [Page hierarchy](../intranet-statistics/valuable-reports.md)
* [Page Titles](../intranet-statistics/valuable-reports.md)
* [Downloads](../intranet-statistics/valuable-reports.md)
* [Browsers](../intranet-statistics/valuable-reports.md)
* [Custom goals](../intranet-statistics/valuable-reports.md)

### Visitor Overview <a id="VisitorOverview"></a>

When launching the intranet, or after an upgrade marketing push or some other call to the intranet, the visitor overview can be a very informative report to get a sense of the overall success of these campaigns. In addition, the visitor overview gives you a high level overview of the health of your intranet. It can serve as an early warning indicator of declining usage allowing you to take the steps necessary to revitalize your intranet.  
  
It should be noted that the "unique visitors" count here is utilizing cookies to track that data. It is not using username to uniquely identify these visits. This page should be used to analyze overall trends, rather then to get exact figures for unique visitors. This report can be found under Visitors &gt; Overview.

![](../../.gitbook/assets/1%20%281%29.png)

### Visits Per Duration <a id="VisitsPerDuration"></a>

By default, Matomo will accurately track the time spent on your pages for all pages, except the last page view of the visit. By default, on the last page view of any visit, Matomo counts the “Time spent on page” as 0 second. And when your visitor views only one page in the website, the visit duration will be set to a default of 10 seconds. This report can be found under Visitors &gt; Engagement.

![](../../.gitbook/assets/2%20%2833%29.png)

### Visits Real-time <a id="VisitsRealtime"></a>

The Live! widget is displayed in the Matomo Dashboard by default, and shows the real time flow of visits to your website. It also displays a real time counter of your visits and page views in the last 24 hours and the last 30 minutes.  
  
The Live! widget refreshes every 5 seconds, and displays new visits \(or existing visitors that view a new page\) at the top of the list with a fade-in effect. For each visitor, you can see all of their attributes:

* date
* number of actions
* time spent on the site
* country
* browser
* operating system
* whether the visitor is new or a returning visit
* the referrer used to access your site \(Search engine & keyword, Campaign, or Referrer website\)
* whether the visitor converted a goal
* If you hover over these icons, you can also see the resolution and the list of enabled browser plugins.

  
The Live! widget also shows the list of page views and actions the visitor performed on your site. Hovering over the icon will show the page name and the time that the page was accessed. Clicking on the icon will open the actual page on your site.

![](../../.gitbook/assets/3%20%2825%29.png)

### Users <a id="Users"></a>

The top users report under the ThoughtFarmer tab on the left hand side menu is one of the great tools to find out who is using your intranet. You can use this report to find out who your intranet champions are. By identifying these individuals you can leverage them as advocates for the intranet and also look at their usage to find out what draws them to the intranet. You can also identify those on the other end of the scale who may need encouragement or training to feel more comfortable using the intranet to its full potential.   
  
**TIP:** The export of the top users report includes additional columns not included in the user interface. It is highly recommended that you use the **export to Excel** version of this report in analyzing data in-depth. This includes added columns for creates and page views per visit \(page views are noted as "hits" in the report\). This gives you added information that will allow you to segment users to find content creators, collaborators, and viewers.   
  
**PRO TIP:** You can apply a weighting to the exported user report in Excel to give a configurable total top user score. In the following example we have removed the unwanted columns and added a row above to hold the weights. The formula for the total in the last column is shown. Using this method you can craft your own unique definition of a top user based on overall activity. Simply re-sort the user list based on the weighted total to get this result.  


![](../../.gitbook/assets/4%20%2819%29.png)

### Search keywords <a id="SearchKeywords"></a>

Knowing what people are searching for will give you an idea of what content keywords are most important to your users. This gives you the opportunity to make important content easier for your users to find by tweaking the subject or title based on common searches.  
  
You can find the search keywords report under the ThoughtFarmer tab on the left hand side menu of your dashboard. Additionally, top search keywords analysis can be done over varying time ranges. For example, if you analyzed the monthly keywords over the course of a year, or over the course of the lifetime of your intranet, you may notice trends in keyword searches that correlate with specific times. For example, terms like "expenses" may come up around the fiscal year end, and terms like "vacation" may come up near summer and winter holidays. Depending on your organization other time related keyword trends can become apparent. This gives you the opportunity to dynamically update the homepage, or other key areas of the intranet, to make this content easier to find when users are looking for it.  
  
The following image shows ThoughtFarmer Analytics search keyword data for a specific day. 

![](../../.gitbook/assets/5%20%283%29.png)

### Page Hierarchy <a id="PageHierarchy"></a>

Finding out the most active areas of your intranet is a very important metric to have. You can use this information to take a number of actions, including:

* Adding quick links on the homepage to popular pages deep in the hierarchy.
* Finding out which groups/sections are the most active and looking for usage patterns that can be utilized in other areas of your intranet.
* Giving this information to content authors to know which sections to target for high visibility of new content.

The Page Hierarchy report found under ThoughtFarmer on the left hand side menu is invaluable for finding out which are the most popular and active sections. The drill down interface allows you to go deep into the hierarchy of your intranet to find out in even more detail which sub-sections and individual pages are being viewed, edited, and commented on the most.  
  
**TIP:** The export functionality in the Page Hierarchy report does not take into account any pages you have drilled down into in the user interface. It simply exports a flat top-level report. However, in IE and Chrome you can highlight and copy areas of the expanded table directly and then paste them into Excel and it will preserve the column and row formatting.

![](../../.gitbook/assets/6%20%2824%29.png)

### Page Titles <a id="PageTitles"></a>

The Page Titles report lists all visited webpages \(with page URLs\). Here you will learn about the number of times each of your websites was visited. There are other important metrics here that you will want to pay attention to: the number of unique pageviews, page creates, edits, comments, bounce rate, average time spent on page, exit rate, and average generation time. This report can be found under ThoughtFarmer &gt; Page Titles

![](../../.gitbook/assets/7%20%2811%29.png)

### Downloads <a id="Downloads"></a>

The Downloads report displays data for unique downloads and downloads, but you can also check the Visitor’s Log for each downloaded file and see what actions led to a particular download. On many websites, you want to track when visitors download a brochure, a photo, a software, etc. Matomo automatically track these clicks as Downloads, and reports them under Behavior &gt; Downloads.  
  
Matomo will automatically detect a download as a click on a link that ends with one of the following file extensions: 7z, aac, apk, arc, arj, asf, asx, avi, azw3, bin, bz, bz2, csv, deb, dmg, doc, docx, epub, exe, flv, gif, gz, gzip, hqx, ibooks, jar, jpg, jpeg, js, mp2, mp3, mp4, mpg, mpeg, mobi, mov, movie, msi, msp, odb, odf, odg, ods, odt, ogg, ogv, pdf, phps, png, ppt, pptx, qt, qtm, ra, ram, rar, rpm, sea, sit, tar, tbz, tbz2, tgz, torrent, txt, wav, wma, wmv, wpd, xls, xlsx, xml, z, zip.

![](../../.gitbook/assets/8%20%2821%29.png)

### Browsers <a id="Browsers"></a>

A report that shows the browsers used to display your intranet the most.  This report can be found on your dashboard as well as under Visitors &gt; Software tab.  


![](../../.gitbook/assets/9.png)

### Custom goals <a id="CustomGoals"></a>

In addition to the built-in reports highlighted above and in the other areas of ThoughtFarmer Analytics, there is another way to add additional tracking that is completely customizable within certain parameters. Custom goals were designed to allow you to identify certain user actions to be tracked as conversions. Please see the page [Set up a goal](../intranet-statistics/set-up-a-goal/).

