# Active Directory Synchronization tasks

### Active Directory synchronization tasks

There are five Active Directory synchronization tasks available:

* **Bulk create users:** This synchronizes the ThoughtFarmer user list with the Active Directory group it is configured to sync with. When a sync occurs, users that are in the AD group but not in ThoughtFarmer have profiles created and field mappings populated.
* **Bulk update users**: This overwrites mapped user fields with the values from the synced AD, when the data owner is AD.
* **Update group page membership from external store groups:** This synchronizes the group page memberships in ThoughtFarmer with their mapped groups in AD.
* **Update security group membership from external store groups:** This synchronizes the security group memberships in ThoughtFarmer with their mapped groups in AD.
* **Bulk deactivate users:** This synchronizes the ThoughtFarmer user list with the Active Directory group it is configured to sync with. When a sync occurs, users that are not in the AD group, or whose accounts are disabled in AD, will be marked as inactive in ThoughtFarmer.

It is important that you verify the membership of the synced with AD group that is configured on the individual Active Directory page found on the **Administration panel: Users & security** &gt; **Employee directory connector** page. If this group is not completely up-to-date in AD then the **Bulk create** and **Bulk deactivate** tasks may add or disable users unintendedly.  
  
If you wish to see which TF groups will have their membership updated using the above AD sync tasks:

1. Go to the **Administration panel: Users & security** &gt; **Group sync** page to view group pages that have their membership synced with external user store groups.
2. Go to the **Administration panel: Users & security** &gt; **Security groups** page to view ThoughtFarmer security groups that have their membership synced with external user store groups.

### AD Photo Sync <a id="section2"></a>

Profile photos can be synced between ThoughtFarmer and Active Directory \(AD\). The sync can be TF to AD or AD to TF. AD has restrictions on profile photos - they must be smaller than 96x96 pixels and smaller than 100 kb. Users can upload profile photos larger than these restrictions, but they will automatically be resized to meet the AD restrictions when the photo sync takes place. This may affect the photo quality in AD and other applications tied to AD. It will not affect the photo quality in TF. AD photo sync does not support animated GIFs as profile photos.

### Daily synchronization <a id="section2"></a>

The AD synchronization tasks can be configured to run daily at a specified time. It is recommended to set this to run at a time when users will not be accessing the intranet. The daily synchronization tasks are set to disabled by default.

![](../../.gitbook/assets/1%20%2885%29.jpg)

#### Configure Active Directory daily synchronization

1. Go to the ThoughtFarmer **Administration Panel**: **Users & security** section &gt; **Employee directory connector** page.
2. Click on the **Active Directory name** for which you want to change the synchronization tasks.
3. Click on the Synchronization Settings ****tab.
4. In the **Daily synchronization** section, click **Create one now** \(or **edit** if there is a sync already setup\).
5. Set the ****synchronization **Run time** in 24 hour format \(local web server time\) using the dropdown menus.
6. Set the synchronization **Frequency** by entering the number of hours between synchronizations.
7. Select the **checkboxes** for the tasks you want to run in the daily synchronization.
8. Click **Save**.

If daily sync is enabled then an additional log trimming task will run by default. This will occur even if no other AD tasks are enabled. This task will clean out all system log entries older then a certain age depending on the type of log entry. This task will delete:

> * ERROR messages older than 6 months
> * WARNING messages older than 2 months
> * INFO and DEBUG messages older than 1 month

### On-Demand synchronization <a id="section3"></a>

Any of the AD synchronization tasks can be triggered at any time using the **On-Demand synchronization** section from the **Administration panel** &gt; **Users & security** section &gt; **Employee directory connector** page. Click on the name of the Active Directory you want to edit and select the **Synchronization Settings** tab.

![](../../.gitbook/assets/2%20%2815%29.jpg)

Simply check the box beside the task\(s\) you wish to run and click **Synchronize now**. The ThoughtFarmer Service will log all information about the tasks in the System Log. You can examine the log to check on task progress and completion.

### Tip: User name changes

If you change a user's name in Active Directory and don't change it in ThoughtFarmer, a new user profile will be created in ThoughtFarmer when the sync tasks Bulk create users and Bulk update users are run. To prevent this, make sure to change the user's name in Active Directory **and** ThoughtFarmer, and then run the sync tasks Bulk create users and Bulk update users before the user tries to log in with their new username.  
  
For more detailed instructions, see [Change a user's name and username](../user-management-1/change-a-users-name-and-username.md).

