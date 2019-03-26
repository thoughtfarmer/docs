# Outgoing email

### Outgoing email

Outgoing email is used by ThoughtFarmer for email notifications. Users can choose in their settings to receive email notifications when certain actions happen on pages they follow. Users can also choose in their settings which of their actions will result in them following pages. For more information, see [Overview of following and notification alerts](../../using-thoughtfarmer/basic-features/following-and-alerts/).

### Configure outgoing email <a id="section1"></a>

Go to the **Administration panel**: **Notifications** section &gt; **Outgoing mail** page.

1. Click **enable** to allow you to enter the following configuration information:

   ![5.5Admin6052OutgoingEmail2.png](https://community.thoughtfarmer.com/imagethumb/837862530000/16693/1000x1000/False/5.5Admin6052OutgoingEmail2.png)

   * **ThoughtFarmer URL**: The URL most users will use to access the site. This is used to format links within email notifications.
   * **From Email Address**: The email address that will be used to send all emails. This does not need to actually exist and should not correspond to the [incoming email](https://community.thoughtfarmer.com/content/105886) address. Best practice is to use a dead-end address like [no-reply@domain.com](mailto:no-reply@domain.com).
   * **Error handling**: Selecting this checkbox will display a text box in which you can enter the domains that are allowed to receive error messages. You can use this feature to prevent people outside of your organization receiving error messages. \(For instance, if there is an error when someone outside your organization tries to add a new comment on the intranet.\)
   * **SMTP server**: The name of the mail server \(e.g. smtp.mailserver.com\)
   * **Port**: The port to access the mail server. The default SMTP port is 25. Secure SMTP uses port 465 by default.
   * **SSL**: Check the box if SSL is required on the mail server.
   * **Username**: Username used for accessing the mail server's SMTP service \(not necessarily required depending on server settings\)
   * **Password**: Corresponding password for user.

2. Click **Save changes** to apply the changes.
3. Go back to the **Outgoing mail** page and click the **Test Connections** button.
4. In the dialog that appears, you can type an email address into the **Test email address** field or leave it as your logged in user's default.
5. Click **Verify**. Any errors in connecting or logging on will be presented in the test results.

![](../../.gitbook/assets/1%20%2888%29.png)

Once both tests are successful and you have received the test email then the outgoing email will be fully configured and operational.

### Notification Timeout <a id="section2"></a>

The notification timeout setting can be configured to reduce the amount of emails sent for similar activity. If the same user edits a page twice a second notification is only sent to all watchers of the page if the second edit occurred _after_ the notification timeout period. To change this setting:

1. Go to the **Administration Panel**: **Advanced options** section &gt; **Configuration settings** page.
2. Type **notification** in the **Search config settings** field to narrow the list of settings.

   ![5.5Admin6052NotificationTimeout2.png](https://community.thoughtfarmer.com/imagethumb/834010130000/16690/1000x1000/False/5.5Admin6052NotificationTimeout2.png)

3. Find the setting notification.email.timeout.
4. Click in the **Value** column beside that setting, and change the value to the desired timeout period \(in minutes\).
5. Click **Save**.

