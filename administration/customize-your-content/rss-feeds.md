# RSS Feeds

### Root RSS Feed page

RSS Feeds bring external news and information on to your intranet via News Cards. Users can bring a stream of external news on to an intranet page by adding RSS News Feed URLs to a News Card in edit mode. Administrators and users with edit permission can access the root RSS Feeds page \(the parent page of all RSS Feeds on the intranet\) by adding **/rssfeeds** to the end of the intranet URL. \(eg. https://myintranet.mycompany.com/rssfeeds\)

![](../../.gitbook/assets/1%20%28128%29.jpg)

### Editing RSS Feeds and posts

From the root RSS Feeds page you can access and edit individual RSS Feed pages which display all the posts for a feed. Edit an RSS Feed page to change the title and summary for that feed. Click the Edit icon \(a pencil\) beside an RSS Feed post to change the title and summary for that post. This will change the titles and summaries wherever the feed or post appears on the intranet. Note that when adding a Feed to a News Card you can add a new title for the Feed. Once the feed is added to the News Card, you cannot edit the title through the News Card, only by editing the RSS Feed page.  
Individual RSS Feed posts can be edited from the News Feed on any intranet page by clicking the External link icon ![8.5Admin29228ExternalLink.jpg](https://community.thoughtfarmer.com/imagethumb/221578130000/16986/44x35/False/8.5Admin29228ExternalLink.jpg)\(an arrow pointing out of a square\) which turns into an Edit icon ![8.5Admin29228Edit.jpg](https://community.thoughtfarmer.com/imagethumb/222513170000/16987/950x950/False/8.5Admin29228Edit.jpg)\(a pencil\) upon hover. Title and Summary can be edited for individual posts, as well as other options like Short Title, Archive Date and Security.  
  
To learn about monitoring External RSS Feeds, see [How to use the External RSS Feed Status Page.](../advanced-configuration/external-rss-feed-status.md)

### Edit templates for RSS Feed pages

There are three templates for pages relating to RSS Feeds that can be edited by going to the **Administration panel**: **User interface** section &gt; **Content type templates** page. Only one template can be created for these pages, but the templates can be edited and have Cards added to them.  
  
The templates are:  
**RSS Post**: Used for the page on which an individual RSS Feed Post lives.  
**RSS News Blog**: Used for the RSS Feed page which is a parent page to all the RSS Feed Posts from that feed.  
**RSS Feeds**: The main root page that is the parent page for all RSS Feed pages on the intranet.  
  
To learn more about editing templates, see [Content Templates](../layout-and-appearance-1/content-templates/) and [Create and modify templates](../layout-and-appearance-1/content-templates/create-and-modify-template/).

### Thumbnail images

When editing an RSS Feed page, you can add a thumbnail image that will display with any posts for that RSS Feed that do not come with an image. You can also add thumbnail images to individual news posts.  
  
**Add a thumbnail image to an entire feed**  
Thumbnail images for entire RSS Feeds will be applied to every feed post that does not have an image already. The feed thumbnail image **will not** override an existing post image.  
  
To add a thumbnail image to an RSS feed, go to the root RSS Feeds page \(the parent page of all RSS Feeds on the intranet\) by adding **/rssfeeds** to the end of the intranet URL. \(eg. https://myintranet.mycompany.com/rssfeeds\) Click on the title of the feed you want to add the image to and go into edit mode on the feed page. In edit mode, click **Add thumbnail** under the Thumbnail heading on the right, or if a thumbnail image already exists, click on the image. For more details about adding Thumbnail images, see[ How to add a thumbnail image](../../using-thoughtfarmer/edit-page-contents/add-thumbnail-images/).  
  
**Add a thumbnail image to an individual post**  
If you set a thumbnail image for an individual RSS Feed Post, it **will** override an existing image for that post. Individual RSS Feed posts can be edited from the News Feed on any intranet page by clicking the External link icon ![8.5Admin29228ExternalLink.jpg](https://community.thoughtfarmer.com/imagethumb/221578130000/16986/44x35/False/8.5Admin29228ExternalLink.jpg)\(an arrow pointing out of a square\) which turns into an Edit icon ![8.5Admin29228Edit.jpg](https://community.thoughtfarmer.com/imagethumb/222513170000/16987/950x950/False/8.5Admin29228Edit.jpg)\(a pencil\) upon hover. Once in edit mode, click **Add thumbnail** under the Thumbnail heading on the right, or if a thumbnail image already exists, click on the image. For more details about adding Thumbnail images, see [How to add a thumbnail image](../../using-thoughtfarmer/edit-page-contents/add-thumbnail-images/).  
 

### Config setting for post images

The configuration setting feeds.images.extractFromContent controls whether the intranet will look for images in the feed post body if an image is not found elsewhere. By default this config setting is set to True, i.e. the intranet will looks for images in the feed post body. If it is set to False, images in the feed body will not be pulled through to the intranet.  
  


