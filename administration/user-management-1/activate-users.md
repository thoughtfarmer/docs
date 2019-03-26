# Activate users



### How to activate user accounts

Users that are marked as "Inactive" in ThoughtFarmer are no longer able to access the site. These accounts can stay inactive for as long as needed. Once the account is ready to be used again you can reactivate it using one of the methods on this page.  
  
For users that are marked as "Profile only" please see [Activate "Profile Only" users.](activate-profile-only-users.md)  
 

### Manually activate Regular, Active Directory, or External users

1.Go to the ThoughtFarmer **Administration Panel**: **Users & security** section &gt; **User management** page.

2.Use the filter, sort, and query tools to find the desired user or set of users \(see [Find users](https://community.thoughtfarmer.com/content/105964) for more info\). 

![](../../.gitbook/assets/1%20%2834%29.png)



3.Select the checkbox beside the desired user\(s\).

4.In the "Choose an action..." dropdown select **Activate user**.

5.Click **Go**.

You can also activate a single user from the **User management** page by clicking the gear icon in the **Action**column on the right, and clicking **Edit account** in the menu that opens.  
  
Uncheck the checkbox "Account is inactive" and click **Save**. The **Edit user account** link is also available to administrators in "Admin mode" when editing a user's profile.

![](../../.gitbook/assets/2%20%2837%29.png)

For AD users; if Automatic User Creation is enabled, then the user's AD account must be active and a member of the synced-to AD group configured on the Employee Directory Connector page. Otherwise, the account will be deactivated if the sync task Bulk inactivate users is run.

### To activate Active Directory users

If AD automatic user creation is enabled then users can be activated automatically using daily AD synchronization tasks. This will activate existing inactive ThoughtFarmer accounts that are active in AD and a member of the synced-to AD group configured on the Employee Directory Connector page. To learn more, see [Active Directory synchronization tasks](../activity-directory-integration/active-directory-synchronization-tasks.md).

![](../../.gitbook/assets/3%20%2816%29.jpg)



#### Activate AD users on-demand

1. Go to the ThoughtFarmer **Administration Panel**: **Users & security** section &gt; **Employee Directory Connector** page.
2. Click on the **Active Directory** that has the users that you want to activate.
3. Click on the **Synchronization Settings** tab.
4. Select the "Bulk create users" checkbox in the **On-demand Synchronization** section.
5. Click **Synchronize now**.

![](../../.gitbook/assets/4%20%2828%29.jpg)

It may take a little time for the [ThoughtFarmer Service](../behind-the-scenes/thoughtfarmer-service.md) to complete the update. This depends on the number of users in the synced-to AD group and the server resources available. Your total licensed user count will change when the update is complete.

