# Use group membership for security



### Use TF group membership to create security groups

You can use the membership of a group page to create a security group, which can then be given permission to view and edit other pages. Group membership must be set to Managed membership, not Open membership, for this to work. This way the group membership is curated, and users cannot just choose to join the group, so the Security group is controlled.  
  
\(Intranet administrators can also use Closed group membership to create security groups. Intranet admins see heading below about Closed membership.\)

### How to use group membership for security

1.Add a new group page. \(See [Create group pages](../add-pages-and-sections/add-a-group-page/create-group-pages.md) for more information.\)

2.Add a group page title. \(This title will also be the name of the Security group that will be created.\)

3.Select the **radio button** for **Managed** membership. \(See [Create group pages](../add-pages-and-sections/add-a-group-page/create-group-pages.md) for an explanation of Open, Managed and Closed membership.\)

![](../../.gitbook/assets/1%20%2851%29.jpg)



4.Click **View / change** and add group members in the Group Members pop-up window. \(To learn more, see [Add & Remove group members](https://community.thoughtfarmer.com/content/105812).\)

5.Select the checkbox **Use as a security group**. This turns off inherited security permissions and creates a Security group that is synced with the group page membership.

6.By default, the Group members are given View only access to the page. To change this to View and Edit permission, click **Edit permissions** and change the setting beside the Security group name in the Security pop-up window, then click **Done**.

7.Continue editing the page or click **Save**.

### Effects of using group membership for a security group

Once the group is created, and the group membership is being used as a security group, that security group will be available to use to give permissions on other pages on the intranet. If a new member is added to the group, that member will be granted permissions on any pages that the security group has permissions on. If a member is removed from the group, they will lose permissions on any pages that they had access to through the security group.

### For intranet admins: using Closed membership to create a Security Group

Closed group membership can also be used to create a TF security group, but only intranet administrators are able to use closed group membership. Closed membership syncs group membership with one or more security groups from Active Directory. If Closed membership is used, if a user is added to the synced AD Security group, they will be added to the synced TF group. If a user is removed from the synced AD Security group, they will be removed from the synced TF group. A user added to the AD security group will receive permissions on any pages the TF security group has been used to give access to. To learn more, see the heading **Sync membership with Active Directory security group** on the page[ Add & remove group members](../add-pages-and-sections/add-a-group-page/add-and-remove-group-members.md).  
  
To create a security group using Closed membership, start by following the steps above. For Step 3, select the **Closed** radio button, then add one or more AD groups from the dropdown menu to sync with the membership. Skip Step 4 and continue with Step 5.

![](../../.gitbook/assets/2%20%2830%29.jpg)



