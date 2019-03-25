# Group sync status

### How to use the Group sync page

The group sync page lists groups that have their membership synced with an Active Directory distribution group and ThoughtFarmer security groups that are synced with AD security groups. It provides information on the "sync health", or whether the group and security group synchronizations are happening the way they should.  
  
For each entry, you see the name of the Active Directory group, the corresponding group page or security group in TF, the date and time of the last sync, and an icon indicating the sync health. If the sync health is good, a green checkmark icon appears. If the sync health is not good, a red X icon appears.

### How to check sync health

1. Go to the **Administration panel**: **Users & security** section &gt; **Group sync** page.
2. Select the tab on the left that you want to check.
3. Look in the **Sync health** column to see the icons indicating sync health.  ![6.7Admin8775SyncHealth.png](https://community.thoughtfarmer.com/imagethumb/171659570000/16781/252x91/False/6.7Admin8775SyncHealth.png)   **OR**   ![6.7Admin8775UnhealthySync.png](https://community.thoughtfarmer.com/imagethumb/173583600000/16782/84x89/False/6.7Admin8775UnhealthySync.png)

Sync health may not be good if nightly sync is not enabled or if the group membership has not been manually refreshed for quite some time.

### How to repair a sync

If the sync health of an AD group is not good, refresh group page membership or security profile membership following the instructions below:

1.Go to the **Administration panel**: **Users & security** section &gt; **Employee directory connector** page.

2.Click on the **Active directory name** for the Active Directory for which you want to refresh the sync.

3.Select the **Synchronization Settings** tab.

4.Under **On-Demand synchronization**, select the checkbox for either "Update group page memberships from external store groups" or "Update security group membership from external store groups", depending on what type of sync needs refreshing.

![](../../.gitbook/assets/2%20%2829%29.jpg)

5.Click **Synchronize now**.

6.Go back to the **Group sync** page to check the sync health.

7.If sync health still isn't good, go to the **Administration panel** &gt; **Logs & statistics** section &gt; **System logs**page and check the system logs for error messages.

For more information, see [group page synchronization](group-page-synchronization.md) or learn [how to enable daily synchronization tasks.](active-directory-synchronization-tasks.md)

  


