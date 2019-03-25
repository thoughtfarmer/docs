# Manage user security groups



### How to manage security group membership for users

The [User Management](./) page allows you to control the security membership to multiple security groups for a single user at one time. To manage security group memberships based on the actual security group please see [Security groups](../security/security-groups.md).

### Manage security profile membership for a user

1. Go to the ThoughtFarmer **Administration panel**: **Users & Security** section &gt; **User management** page.
2. Use the filter, sort, and query tools to find the desired user or set of users \(see [Find users](find-users.md) for more info\).
3. Click the **gear icon** in the **Action** column to the right of the user, and click **Security groups** in the menu that opens. This will open the **Select a security group** dialog box.

![](../../.gitbook/assets/1%20%2822%29.jpg)

4.Drag-and-drop security groups from the **All security groups** column to the **Member of** column to add a user to that group.

* To select multiple consecutive groups: Click on the first group, then hold the SHIFT key and click on the last group.
* To select multiple non-consecutive groups: Click on the first group, then hold the CTRL key and click on each group you want to select.
* Once multiple groups are selected, click on any of the selected groups to drag-and-drop the entire selected group to another column.

5.Drag-and-drop security groups from the **Member of** column to the **All security groups** column to remove a user from that group.

6.Click **Save**.

Note that you cannot add or remove users from security groups that are mapped to Active Directory security groups. These will be noted with a lock icon beside them. You must change the membership in Active Directory and then run the sync task [Refresh security group memberships from AD groups](../activity-directory-integration/active-directory-synchronization-tasks.md).

