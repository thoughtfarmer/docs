# Show/Hide page owner in header

### Choose to show or hide the page owner name in the page header

By default, the name of the page owner and the date the content was created or last updated shows on pages, posts and forum topics. You can hide the page owner name and date on any or all of those content types if desired. If you wish to have the page owner name and date display on other content types, contact ThoughtFarmer Support for assistance.  
  
**Page header with page owner name and updated date showing:**

![](../../../.gitbook/assets/1%20%28127%29.jpg)

**Page header with page owner name and date hidden:**

![](../../../.gitbook/assets/2%20%283%29.jpg)



Changing the configuration setting below only affects pages that are created after the change is made. You can choose to show or hide the page owner in the page header on an individual page basis in edit mode. If you need to change this option for many pages that already exist, contact ThoughtFarmer Support for assistance.  
  
Change whether the page owner name and date shows in the header with this configuration setting:

1. Go to the **Administration panel**: **Advanced options** section &gt; **Configuration settings** page.
2. Type **owner** in the **Search config settings** field to narrow the config settings results.
3. Find the config setting page.header.showOwnerInfoByDefault.
4. Click in the **Value** column beside the config setting. If you want to **hide** the page owner and date from a Content Type:
   1. **Pages**: Remove the "1" from the comma-separated value list.
   2. **Posts**: Remove the "11" from the comma-separated value list.
   3. **Forum Topics**: Remove the "26" from the comma-separated value list.
   4. To **show** the page owner and date on a Content Type, **add** the appropriate value to the comma-separated value list.
5. Click **Save**.

