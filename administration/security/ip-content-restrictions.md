# IP Content Restrictions

### How IP Restrictions Work

IP restrictions use a top-down approach when evaluating configured IP ranges. This means that pages higher up in the intranet heirarchy that contain IP content restrictions will override pages lower down in the heirarchy.  
  
Example:

![](../../.gitbook/assets/1%20%2888%29.png)

A page on the intranet, /content/123, has an IP content restriction. Another page, /content/456, which is a child of /content/123, also has an IP content restriction. In this case, the IP content restriction rules for /content/123, which is higher up in the heirarchy, will _**supercede**_ the rules configured for /content/456, _**even if the /content/456's rules contradict /content/123's**_.  
  
So, in the image above, even though /content/456 allows IP addresses between 123.234.12.0 - 123.234.12.255, access to that page will be denied due to the fact that the parent page, /content/123, defines a more restrictive rule than /content/456.  
  
When a search is performed, all content is indexed and included in total item counts, even when IP restrictions are in effect. Restricted content will not be displayed to users outside of the specified range, however it will be included in the item counts in search results, forum pages, etc. This means that the number of items actually displayed in the search results may not match the item counts shown.  


![](../../.gitbook/assets/2%20%2839%29.jpg)

### Enable IP Content Restrictions

The first step to configuring IP content restrictions is to enable it. To do this, navigate to the **Administration panel**: **Advanced options** section &gt; **Configuration settings** page and set the **ip.content.restrictions.enabled**setting to **true**. This will add the additional administrative option **IP content restrictions** under the **Users & Security** section of the **Administration panel**.  
 

### Adding IP Content Restrictions

To add IP content restrictions to pages, navigate to the **Administration panel**: **Users & Security** section &gt; **IP content restrictions** page. To add a new IP range, click the **Add IP range** button in the section you want - Administration pages or regular pages. When this button is clicked, a dialog appears allowing you to select the following settings for the page you want to restrict.

* **Page**: The page you want to restrict. _**Note**_: you cannot restrict access to the top content page \(dashboard or content/1\), or the people directory.
* **Allowable IP ranges**: One or more allowable IP ranges. This feature uses [CIDR](http://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing) notation to specify IP ranges, similar to how firewalls configure IP ranges.

![](../../.gitbook/assets/3%20%2849%29.png)

You can add one or more sets of ranges to restrict access from different IP ranges.

