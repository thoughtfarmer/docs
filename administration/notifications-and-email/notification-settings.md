# Notification settings

### Change settings for individual users

Users can change their notification settings at any time. To do this, a user clicks on their **name or profile photo** in the top right of the Application Toolbar and clicks **Settings** in the dropdown menu. The user can then change the checkbox options under the **Notification Settings section** for Auto-follow, Emails and Summary emails, and click **Save** to save the changes.  
  
Administrators can also change these Settings for a specific user. To do this, an administrator goes to the **user's profile page**, clicks the **down arrow** in the **Page Controls**, and clicks **Settings** in the options that appear. The administrator can then change the checkbox options under the **Notifications Settings section** and click **Save** to save the changes for that user.  
  
The following settings affect Notification settings for all intranet users.

### Daily Email Check-up and Weekly Email Newsletter setting

Daily Email Check-ups and Weekly Email Newsletters are sent out to give intranet users a summary of activity on the intranet and intranet pages that are popular that week. Administrators can choose whether new users will receive these emails by default. Individual users can choose whether to receive the daily and weekly emails by editing the notifications tab of their profile settings.  
  
To change the **Daily Email Check-up** settings:

1. Go to the **Administration panel**: **Notifications** section &gt; **Automated Email Newsletter settings** page.
2. Under the **Daily Email Check-up settings** heading, check the box to enable daily emails.
3. Click on the time of day to open the dropdown menu, and select the time when you want the email to be sent.
4. Select the number of items to display in the email from the dropdown menu.
5. Select the radio button for the default setting you want for new users.
6. Click **Save changes**.

To change the **Weekly Email Newsletter** settings:

1. Go to the **Administration panel**: **Notifications** section &gt; **Automated Email Newsletter settings** page.
2. Under the **Weekly Email Newsletter settings** heading, check the box to enable daily emails.
3. Click on the day of the week and time of day to open the dropdown menus, and select the day and time when you want the email to be sent.
4. Select the number of items to display in the email from the dropdown menu.
5. Select the number of popular items to display in the email from the dropdown menu.
6. Select the radio button for the default setting you want for new users.
7. Select the checkbox if you want to "Hide top level navigation pages from the popular pages section of the Weekly Email Newsletter".
8. Click **Save changes**.

To set all users to receive the daily or weekly digests, click "Set to all" under the appropriate section.  
To set all users to not receive the daily or weekly digests, click "Reset to none" under the appropriate section.

### Configuration settings for notifications

To access the configuration settings that affect notifications:

1. Go to the **Administration panel**: **Advanced options** section &gt; **Configuration settings** page.
2. Type **notification** in the **Search config settings** field to narrow the config settings results.
3. Find the config setting you want to change.
4. Click in the **Value** column beside the config setting and change the value of the setting in the box that appears.
5. Click **Save**.

### Change length of time before another notification email is sent

Change the config setting notification.email.timeout to the time in minutes that you want to elapse between notifications about changes to the same page/file/folder. This setting applies to page adds and edits, not to comments, archiving/restoring, following, etc.

### Change how many notifications show in menu

Change the config setting notifications.overlay.numberOfItems to the number of notifications that you want to show in the notifications menu on the application toolbar. As new notifications appear, they will replace older notifications, so only the specified number of notifications shows in the menu.

### Change length of time between checking for new Alerts

Administrators can control how often the intranet checks if users have new Alerts \(Notifications/Mentions\). When a user has new Alerts, this is signified by a red dot containing the number of new Alerts shown in the Alerts menu.  
  
Change the config setting notifications.pollingInterval to the time in minutes that you want to elapse between checking for Alerts. The default setting is 15 minutes.

