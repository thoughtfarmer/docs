# SuperNav setting

The SuperNav \(sometimes called the Left Navigation Card\) is the Card on the left side of all intranet pages. It shows where the current page lies in the intranet structure, and lets you search subpages and navigate to pages anywhere on the intranet.  
  
This page explains available settings for customizing the SuperNav. To learn more about general use of the SuperNav, see [Use the SuperNav](../../../using-thoughtfarmer/search/use-the-supernav.md).

### Hide People, Groups, or News pages from SuperNav

You may want to hide the default People, Groups or News pages that show by default in the SuperNav, as they also show by default in the Main Navigation Bar. You can also hide links to these top level pages in the Main Navigation Bar instead. \(To learn more, see the section about hiding top level pages on the page [Main Navigation Bar](main-navigation-bar.md).\)  
  
**Default pages showing in the SuperNav**

![](../../../.gitbook/assets/1%20%28113%29.jpg)



1. Go to the **Administration panel** &gt; **Advanced options** section &gt; **Configuration settings** page.
2. Type **supernav** in the **Search config settings** box to narrow your options.
3. Depending on the page you want to hide, find the appropriate config setting:
   1. **Groups:** navigation.supernav.showGroups
   2. **News:** navigation.supernav.showNews
   3. **People \(Employee directory\):** navigation.supernav.showPeople
4. Click in the **Value** column beside the config setting. A box will open.
5. Select **false** to hide the page from the SuperNav. \(Select **true** to show the page in the SuperNav.\)
6. Click **Save**.

### Hide SuperNav from homepage on desktop

Some administrators may wish to hide the SuperNav \(Left Navigation Card\) from the homepage on desktop computers. Note that it will still appear on other intranet pages. On smartphones and sometimes on tablets, the Main Navigation Bar does not show because of space limitations, therefore it is necessary to have access to the Left Navigation, and it cannot be removed from these devices. On these devices the Left Navigation is hidden, but can be accessed by clicking the hamburger icon \(three horizontal lines\) on the left of the Application Toolbar at the top of the page.

1.Click on the **gear icon** on the right of the Main Navigation Bar.

![](../../../.gitbook/assets/2%20%2888%29.jpg)



2.Click on **Edit homepage** in the menu that opens.

3.Click **Set up cards** on the right under **Content type & template.**

4.In the **Card setup window** that appears, find the **Left Navigation** **Card**.

![](../../../.gitbook/assets/3%20%2825%29.jpg)



1. Select the checkbox **Hide for desktop**.
2. Click **Done** in the bottom right of the **Card setup window**.
3. Click **Save** on the top right.

### Collapse SuperNav breadcrumb

The SuperNav shows a breadcrumb trail to the current page you are viewing. If you have many levels in your page hierarchy, this will result in a long breadcrumb. You can choose to collapse the breadcrumb when it reaches a certain number of levels through a configuration setting. When you choose to have the breadcrumb collapse, all levels between the homepage and the current page will be collapsed.  
  
If you find that your organization has become overwhelmed with too many levels in your intranet hierarchy, please contact [ThoughtFarmer Support](mailto:helpdesk@thoughtfarmer.com) to discuss how we can help.  
 

1. Go to the **Administration panel** &gt; **Advanced options** section &gt; **Configuration settings** page.
2. Type **supernav** in the **Search config settings** box to narrow your options.
3. Find the setting navigation.supernav.breadcrumbCollapsePoint.
4. Click in the **Value** column. A box will open.
5. In the text box, type the number of page levels at which point you want the breadcrumb to collapse.
6. Click **Save**.

**Regular SuperNav and Collapsed SuperNav**

![](../../../.gitbook/assets/new%20%282%29.jpg)



