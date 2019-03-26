# Discussion capture

### Discussion Capture

Discussion Capture pages are synced with a distribution group or mailing list. Once configured, all email messages sent to the group are captured and stored within ThoughtFarmer.

### Enable/Disable Discussion Capture

Discussion Capture is disabled by default on new installs. Once you enable Discussion Capture, a new admin page appears at the **Administration panel**: **Notifications** section &gt; **Discussion capture** page.

1. Go to the **Administration panel**: **Advanced options** section &gt; **Configuration settings** page.
2. Type **capture** in the **Search config settings** field to narrow the config settings results.![6.7Admin8677EnableDiscussionCapture.png](https://community.thoughtfarmer.com/imagethumb/846233600000/16487/600x600/False/6.7Admin8677EnableDiscussionCapture.png)
3. Find the config setting discussionCapture.enabled
4. Click in the **Value** column beside the config setting. The default setting is false.
   1. Select **true** if you want to enable Discussion Capture.
   2. Select **false** if you want to disable Discussion Capture.
5. Click **Save**.

### Create a Discussion Capture page

You can create a Discussion Capture page with any mail or distribution list. This can be an external mailing list run through a 3rd party such as Gmail. All that is required is that you can access the settings for the mailing list in order to add addresses.  
  
Before you begin, incoming email must be enabled. Check the [Incoming email](https://support.thoughtfarmer.com/content/105886) page. You will need this email address for configuring Discussion Capture.

1. Add the email address from your intranet's incoming mail screen \(**Administration panel**: **Notifications** section &gt; **Incoming mail** page\) to the mail or distribution group.
2. Add a page in the navigation where you want the Discussion Capture page to be.
3. In Edit mode, click on the **Content type** dropdown under the **Content type & template** heading on the right. Select the **Mailing list** content type from the menu that opens.
4. Enter the mailing list email address in the **Mailing list email address** text box.
5. The checkbox **Archiving enabled** is selected by default. Deselect it if you do not want to automatically archive the emails.
6. Add content to the page if desired and click **Publish**.

After adding a Mailing List page, you will be able to see the new page listed on the **Administration panel: Notifications** section &gt; **Discussion capture** page. On this page you can choose at any time whether or not a mailing list's emails are captured and archived by clicking **enable** or **disable** in the **Archiving** column.  


