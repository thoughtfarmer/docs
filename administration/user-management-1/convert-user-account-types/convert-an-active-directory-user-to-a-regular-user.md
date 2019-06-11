# Convert an Active Directory user to a Regular user



### How to convert an Active Directory user to a Regular user

You can change any Active Directory user to a Regular user at any time. This does mean that the AD integration features for this user will no longer apply \(e.g. AD field mappings, group sync\). The benefit is that the user no longer requires a Microsoft Client Access license and can use the password recovery feature if necessary.

#### Before you begin

Ensure that you have set up, or are able to set up a Forms authentication route. Regular users are required to use this authentication mechanism. Please see Configuring authentication routes for more information.

### Convert an Active Directory user to a Regular user

1.Go to the ThoughtFarmer **Administration Panel**: **Users & security** section &gt; **User management** page.

2.Use the filter, sort, and query tools to find the desired user \(see [Find users](../find-users.md) for more info\).

3.Click the gear icon in the **Action** column to the right of the user, and click **Edit account** in the menu that opens.

![](../../../.gitbook/assets/3%20%2847%29.png)

4.Change the **Account type** radio button to **Regular user**.

![](../../../.gitbook/assets/2%20%2829%29.jpg)

5.Enter a username in the provided text field.

6.In the **Password** section, reset the user's password by specifying a temporary password in the **Reset password** field.

![](../../../.gitbook/assets/4%20%2844%29.png)

7.Click **Save.**

You can now send the user their login username and password manually. They will be required to change this password the next time they log in. If you do not need the user to change their password on next login you can cancel this by using the [Cancel force password change](https://community.thoughtfarmer.com/content/105892) action on the [User Management](https://community.thoughtfarmer.com/content/105965) page.

