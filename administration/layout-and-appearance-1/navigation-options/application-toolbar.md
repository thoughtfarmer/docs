# Application Toolbar

### Application Toolbar

![](../../../.gitbook/assets/1%20%2879%29.png)



The Application Toolbar is the top bar on every page of the intranet. It allows easy access to a user's homepage, profile page, Bookmarks, page History, Groups, and Alerts from any page. Users see a list of any files they have locked for editing, and can check the files back in from the Toolbar. There is direct access to Help information, the Edit profile page, and the option to show or hide archived content from the menu on the right of the Application Toolbar.   
  
Administrators enter and leave admin mode and access the Administration panel via the menu that drops down when you click on your name or profile photo on the right of the Application Toolbar.  
  
For more information, see end user instructions on [how to use the Application Toolbar](../../../using-thoughtfarmer/basic-features/application-toolbar.md).

### Configure settings for the Application Toolbar

The Administration panel contains several options for customizing the Application Toolbar. These relate to the Toolbar's appearance, and the options available from the Toolbar.  
  
To change the following settings:

1.Go to the **Administration panel** &gt; **Advanced options** section &gt; **Configuration settings** page.

2.Type **toolbar** in the **Search config settings** field to narrow the list of settings.

![](../../../.gitbook/assets/2%20%2837%29.png)



3.Find the desired setting, and click in the **Value** column beside it to change the setting.

4.Click **Save**.

For more details, see the individual instructions for each setting below.

### Display Bookmarks in Toolbar

Administrators can choose whether or not to have Bookmarks display in the Application Toolbar. Bookmarks can also be displayed on pages in the Bookmark manager Card. If History is also enabled, Bookmarks and History share a menu on the Toolbar, each with their own tab. The tab that was used last determines the title of the menu in the toolbar.

1. Go to the **Administration panel** &gt; **Advanced options** section &gt; **Configuration settings** page.
2. Type "toolbar" in the **Search config settings** field to narrow down the configuration settings.
3. Find the config setting applicationToolbar.bookmarks.enabled, click in the **Value** column beside that setting, and click the radio button beside the desired value:
   1. Select **true** to have Bookmarks show in the Application Toolbar
   2. Select **false** to remove Bookmarks from the Application Toolbar.
4. Click **Save**.

### Display Your Groups in Toolbar

Administrators can choose whether or not to have the Your Groups menu display in the Application Toolbar. Users can access the group pages for all of the groups they belong to from the Your Groups menu.

1. Go to the **Administration panel** &gt; **Advanced options** section &gt; **Configuration settings** page.
2. Type "toolbar" in the **Search config settings** field to narrow down the configuration settings.
3. Find the config setting applicationToolbar.groups.enabled, click in the **Value** column beside that setting, and click the radio button beside the desired value:
   1. Select **true** to have Your Groups show in the Application Toolbar
   2. Select **false** to remove Your Groups from the Application Toolbar.
4. Click **Save**.

### Choose Help URL

Users can access intranet help by clicking on their name or profile photo at the right of the Application Toolbar and selecting Help in the menu that opens. The default Help URL is [http://www.thoughtfarmer.com/support/](http://www.thoughtfarmer.com/support/), the location of ThoughtFarmer's public intranet support documents.  
  
Administrators can choose an alternate Help URL if they wish. Your organization may have created help pages or tutorials unique to your needs, independently or with the help of ThoughtFarmer's Support Team. To change the Help URL:

1. Go to the **Administration panel** &gt; **Advanced options** section &gt; **Configuration settings** page.
2. Type "toolbar" in the **Search config settings** field to narrow down the configuration settings.
3. Find the config setting applicationToolbar.help.url, click in the **Value** column beside that setting, and enter the URL that you wish the **Help** option to direct to.
4. Click **Save**.

### Display History in Toolbar

Administrators can choose whether or not to have a History of recently viewed intranet pages display in the Application Toolbar. If Bookmarks are also enabled, Bookmarks and History share a menu on the Toolbar, each with their own tab. The tab that was used last determines the title of the menu in the toolbar.

1. Go to the **Administration panel** &gt; **Advanced options** section &gt; **Configuration settings** page.
2. Type "toolbar" in the **Search config settings** field to narrow down the configuration settings.
3. Find the config setting applicationToolbar.recently.viewed.pages.enabled, click in the **Value** column beside that setting, and click the radio button beside the desired value:
   1. Select **true** to have History show in the Application Toolbar
   2. Select **false** to remove History from the Application Toolbar.
4. Click **Save**.

### Change number of pages in History

Administrators can control the maximum number of pages that display when History is viewed in the Application Toolbar.

1. Go to the **Administration panel** &gt; **Advanced options** section &gt; **Configuration settings** page.
2. Type "toolbar" in the **Search config settings** field to narrow down the configuration settings.
3. Find the config setting applicationToolbar.recently.viewed.pages.count, click in the **Value** column beside that setting, and enter the maximum number of recently viewed pages to show in the Application Toolbar.
4. Click **Save**.

