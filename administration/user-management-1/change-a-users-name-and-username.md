# Change a user's name and username



### How to change a user's name and username

Sometimes a user changes his or her name because of marriage, divorce or for other reasons. Administrators can change a user's name and username so that all of the user's actions and content on the intranet are retained in the user's profile, but using the new name and username.  
  
If this change is for a **Regular user**, the name and username can be managed through the [User Management](./)page. The old username will immediately become invalid once this action is complete.  
  
If this change is for an **Active Directory** user then the name and username must be changed in AD first. It must then also be changed in ThoughtFarmer before the user attempts to log in or the [bulk create user ](../activity-directory-integration/active-directory-synchronization-tasks.md)AD task is run. Otherwise, a new ThoughtFarmer profile will be created in addition to the existing profile under the previous name.

### To change a user's name or username:

1. If the user is an Active Directory user, change the user's name and username in Active Directory. Remember to update the user's email address as well if needed. If the user is not an Active Directory user, go to Step 2.
2. Go to the ThoughtFarmer **Administration Panel**: **Users & security** section &gt; **User management** page.
3. Use the filter, sort, and query tools to find the desired user \(see [Find users](find-users.md) for more info\).
4. Click the **gear icon** in the **Action** column to the right of the user, and click **Edit account** in the menu that opens.

![](../../.gitbook/assets/1%20%28111%29.png)

5.Enter the new username in the **Username** text field in the **Account Type** section. For an Active Directory user, the username must correspond exactly to what has been entered in Active Directory.

![](../../.gitbook/assets/2%20%2884%29.png)

6.Enter the new **First name** and/or **Last name** in the text fields under the **Account information** section. For an Active Directory user, the First name and Last name must correspond exactly to what has been entered in Active Directory.

![](../../.gitbook/assets/3%20%2847%29.png)

7.Click **Save**.

8.To complete the change, either wait for the next scheduled AD synchronization to run, or trigger an on-demand sync. If a user tries to log in with their new username before they sync is run, the user will receive an incorrect username/password message and will be unable to log in.

1. To trigger an on-demand sync, go to the **Administration panel: Users & security** section &gt; **Employee directory connector** page.
2. Click on the appropriate **AD**.
3. Click on the **Synchronization Settings** tab.
4. Select the checkboxes for the tasks **Bulk create users** and **Bulk update users** under the **On-demand synchronization** section.
5. Click **Synchronize now**.

### Tip: Change user settings

Administrators can change certain user settings on a user's profile page. To do this, go to the **user's profile page**, click the **down arrow** on the right of the of the **Page Controls**, and click **Settings** in the options that appear. An administrator can then change settings about timezone, archiving, alternate email and notifications for that user.  


