# Security groups

### Manage page security through Security groups

ThoughtFarmer allows you to manage page security using Security groups. This allows for specific sets of users to be easily added to the security settings for any page in the Security dialog. On each page you can give permission for individual users or groups of users to View & edit, or View only. If no permissions are given, users will be unaware that a page even exists.  
  
To learn how to apply security settings to pages, see [How to change permissions to view & edit.](../../using-thoughtfarmer/security-settings-and-permissions/permission-to-view-and-edit.md)  
  
**Go to**:

* [Managing security groups](security-groups.md)
* [System Groups](security-groups.md)
* [Active Directory Mapped Groups](security-groups.md)
* [Regular Security Profiles](security-groups.md)

### Managing Security Groups <a id="section1"></a>

To manage security groups, go to the **Administration panel**: **Users & security** section &gt; **Security groups** page.  
  
Security Groups are divided into three subtypes and have different options for configuration. They are:

* System Security Groups
* Security Groups - includes Regular and Active Directory Mapped Groups
* Security Groups linked with Group Pages

For all types of security groups, clicking the number in the **Securing** column brings up a list of the pages that the security group has been given explicit permissions on.

### System Security Groups <a id="section2"></a>

There are three system security groups in ThoughtFarmer whose membership cannot be edited.

![](../../.gitbook/assets/1%20%2884%29.jpg)

#### Guests

Contains only the guest user. This is the user that all guests log in as. This security group allows for management of what guests can and cannot access. Guests can never have "View and Edit" access.

#### Administrators

This security group contains all users that are currently in Admin mode. This group is used internally and is not able to be managed on a content by content basis. All users in the Admin security group have "View and Edit" access to all content when they are in Admin mode.

#### All Registered Users

This security group contains all users that actually have a profile in ThoughtFarmer. Anytime a user is created they are automatically added to this group. The default page security on a blank install sets the owner of a page with "View & Edit" permissions and All Registered Users with "View only" permissions. Once permissions throughout the site are modified this will be dependent on permission inheritance.

### Editing security groups

There is only one configuration option when you click **Edit** beside the system profiles; this is whether to display the group in the [Security](./) pop-up window used for changing security settings. You are also shown a list of all pages the group currently has explicit permissions on. Explicit permissions means all top level permissions that have been deliberately applied, rather than implicitly through page security inheritance. The list of pages shows for all security group types.

### Active Directory mapped security groups <a id="section3"></a>

In order for security groups to be mapped to Active Directory \(AD\) groups, AD integration must be enabled on the Login provider page. The AD mapped group will show the name of the security group followed by the name of the mapped to AD group in brackets.  
  
To create a new AD mapped group: Click **Add security group** under **Security groups**. Type in a **Group name**and select **Map members from Active Directory group**. Selecting the checkbox **Display in security settings**allows the new group to be displayed in the security settings dialog for a page. If AD configuration settings are correct, you should be able to select from a dropdown box with a pre-populated list of all available Security Groups in your Active Directory.

![](../../.gitbook/assets/2%20%2875%29.jpg)

Click **Save group**. Once you save the new security group all members will be imported from the AD membership for that group.  
  
You can edit an existing group by clicking **Edit** under the **Action** column beside the group. This allows you to change the name, the mapped group, and to toggle the display mode for the Security settings dialog. You can also choose to select members manually. This will keep all current members but the group will become a **Regular security group** \(see below\).  
  
On an AD mapped group, clicking the number in the **Members** column brings up a list of current members. For security reasons AD is always considered the master for membership of security groups. You cannot edit membership from ThoughtFarmer. To alter membership you will need to change membership in the correct AD security group and then wait for the daily scheduled tasks to run \(if configured\), or perform an **On-Demand Synchronization**. Simply clicking **Edit** and **Save group** on an AD mapped security group will trigger a re-sync with AD membership.  
  
See [Active Directory synchronization tasks](../activity-directory-integration/active-directory-synchronization-tasks.md) for more information on the above-mentioned synchronization tasks.  
 

### Regular security groups <a id="section4"></a>

Regular security groups can be created the same way as AD mapped profiles except that you choose the option **Select members manually** when creating them. In this way you can manage membership of these security groups from ThoughtFarmer. On a regular security group, clicking the number in the **Members** column dialog box that lets you manually select security group membership as you would in a security permissions dialog.

![](../../.gitbook/assets/3%20%2867%29.jpg)

As with an AD mapped security group, you can edit the configuration at any time. However, when you switch a regular security group to an AD mapped security group and save, all previous membership is lost and the security group now contains the membership as it is in the mapped to AD group.

### Security Groups linked with Group Pages

Security Groups linked with group pages are created when a page editor selects the checkbox **Use as a security group** when editing a group page. These Security Groups are not created from the Administration panel. The membership of these Security Groups is controlled by adding or removing members on the group page.

![](../../.gitbook/assets/4%20%2842%29.jpg)

A configuration setting controls whether the **Use as a security group** checkbox appears on group pages \(and thereby controls whether group membership can be used for security groups\). Set the configuration setting groups.canUseAsSecurityGroup to **true** to allow using group membership for security, and set to **false** to disallow using group membership for security.  
  
On the Security Groups Admin page, administrators can view which members are in a security group linked to a group page by clicking the number under the **Members** column. They can also view which pages the security group has been given explicit permissions on by clicking the number under **Securing**.  
  
To learn more about security groups linked with group pages, see [Use group membership for security.](../../using-thoughtfarmer/security-settings-and-permissions/use-group-membership-for-security.md)  


