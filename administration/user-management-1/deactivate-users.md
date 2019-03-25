# Deactivate users



### How to deactivate user accounts

Users that are marked as "Inactive" in ThoughtFarmer are no longer able to access the site. They are not listed in the Employee Directory except to administrators in "Admin mode." Any content that they own \(pages, attachments, comments\) is still accessible and seen by other users. However, the owner is flagged as inactive, and users do not have a link to that user's profile page. While content owned by inactive users shows up in search results for all users, only administrators in Admin mode see search facets for inactive users \(eg. edited by, owned by\).

### Manually deactivate Regular, Active Directory or External users

1.Go to the ThoughtFarmer **Administration Panel**: **Users & security** section &gt; **User management** page.

2.Use the filter, sort, and query tools to find the desired user or set of users \(see [Find users](find-users.md) for more info\).

![](../../.gitbook/assets/1%20%2810%29.png)

3.Select the checkbox beside the desired user\(s\).

4.In the "Choose an action..." dropdown select **Deactivate user**.

5.Click **Go**.

You can also deactivate a single user from the **User management** page by clicking the gear icon in the **Action**column on the right, and clicking **Edit account** in the menu that opens. Select the checkbox "Account is inactive" and click **Save**. The **Edit user account** link is also available to administrators in "Admin mode" when editing a user's profile.  
  
_For AD users_; if [Automatic User Creation](../activity-directory-integration/active-directory-basic-settings/) is enabled, then the user's AD account must be inactive/deleted or removed from the synced-to AD group configured on the Employee Directory Connector page. Otherwise, if the user tries to log in again the account will be reactivated.

### Automatically deactivate Active Directory users

If AD automatic user creation is enabled then users can be deactivated automatically using daily [AD synchronization tasks](../activity-directory-integration/). This will deactivate ThoughtFarmer accounts that are inactive/deleted in AD or removed from the synced-to AD group configured on the Employee Directory Connector page.

### Manually deactivate multiple Active Directory users

1. Go to the ThoughtFarmer **Administration Panel**: **Users & security** section &gt; **Employee Directory Connector** page.
2. Click on the **Active Directory** that has the users you want to deactivate.
3. Click the **Synchronization Settings** tab.
4. Select the **Bulk deactivate users** checkbox in the **On-demand Synchronization** section. 

![](../../.gitbook/assets/2%20%2821%29.jpg)

5.Click **Synchronize now**.

It may take a little time for the [ThoughtFarmer Service](../behind-the-scenes/thoughtfarmer-service.md) to complete the update. This depends on the number of users in the synced-to AD group and the server resources available. Your total licensed user count will change when the update is complete.  


