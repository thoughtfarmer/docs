# Search setting

### Change Search settings in the Admin panel

This page explains settings that can be changed using the **Administration panel**: **Search** section &gt; **Search settings** page.  
  
These include:

* The number of search results that display on the main search page and People or Group Directories
* The number of results that display on forum pages or the main polls page
* The number of search filter facets that display
* Page types that will be excluded from search results
* The number of Best Bets that will display
* The number of Suggestions that will display
* Words that will be excluded from search terms
* Pages that will be excluded from search results
* Other advanced search settings

### **Index**

If you encounter problems with search functionality, the actions on this page may help you to resolve the problem. To learn more, see [Search Index.](untitled-2/)

### **Page Sizes**

These values determine the number of results that will display on a page at once. If the number of results is greater than the set value, the results will display on multiple pages that users can navigate between. This value can be any number you like, but a maximum of 100 is suggested to maintain good performance.  
  
The settings apply to the following:  
**General:** Main search page results  
**Forum:** List of forum posts on forum pages  
**People:** People/Employee Directory search results  
**Groups:** Groups Directory search results  
**Polls:** List of polls on main poll page  
  
To change a page size setting, click in the corresponding box, type in the new value and click **Save** beside the box.  
  
**Example:**  
**A search for "pacific" yielded 107 results. Because the Main search page size is set to ten, only ten results display on the page at once.**

![](../../.gitbook/assets/1%20%2880%29.jpg)

  
**Page numbers at the bottom allow users to navigate between the 107 search results.**  
![8.1Admin16745PageNumbers.jpg](https://community.thoughtfarmer.com/imagethumb/163836370000/16977/361x80/False/8.1Admin16745PageNumbers.jpg)

### **Facets**

These settings control the number of search facets that appear for each filter type in the filter card. If there are more facets than the set number, a search box will appear at the end of each type of facet to allow users to search for facets that are not listed.  
  
**In this example, the Edited by and Owned by filter types are set to five facets each.**

![](../../.gitbook/assets/3%20%2824%29.jpg)

To learn more, see [Configure tag display on search](untitled-5/configure-tag-display-on-search.md).

### **Page Types**

Select the checkbox beside page types that you want to be excluded from general search results.

### **Best Bets**

This setting determines the maximum number of Best Bets that will display on a search, as configured on the **Administration panel**: **Search** section &gt; **Best Bets** page. To learn more, see [How to use Best Bets](untitled-9.md).  
  
**A search for "cell phone" has been set up to return a Best Bets result about mobile banking**

![](../../.gitbook/assets/4%20%2841%29.jpg)

### **Functions**

Although a brief description of this section is provided, we strongly recommend contacting ThoughtFarmer Support for more information before making any changes to these settings.  
  
**Calendar events**  
Events in the past have decreased relevance - the older it is the less relevant it is. ThoughtFarmer uses a Gaussian date decay function for calendar event decay. The **Decay rate** affects how quickly the score decays \(per interval\). The **Decay scale** controls the decay interval.  
  
**Page type**  
Certain page types have their scores adjusted by these values - think of it as a multiplier.  
  
**Popularity**  
**Weight** controls how much of an effect popularity has on page relevance - think of it as a multiplier.

### **Suggestions**

This setting has to do with the **Did you mean?** feature of search which suggests other words if it thinks a user has misspelled their search term.

![](../../.gitbook/assets/5%20%2824%29.jpg)

**Number to show** determines the number of suggestions that will display when Search+ thinks that a user has misspelled the search term. **Max score** means suggestions will only be shown when the max score of the search results returned is below this value. If you want suggestions to show more frequently, make the value higher; if you want suggestions less frequently, make the number lower.  


### **Stopwords**

This is a list of words that will be ignored if they are included in search queries. By default, such common words as **and**, **but**, and **to** are ignored. Administrators can add or delete stopwords for each enabled language on the intranet.

### **Exclusions**

Add pages to this list to exclude them \(and any subpages\) from the main site-wide search.

