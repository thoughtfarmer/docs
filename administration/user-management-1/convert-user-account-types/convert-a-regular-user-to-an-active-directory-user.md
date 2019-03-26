# Convert a Regular user to an Active Directory user



### How to convert a Regular user to an Active Directory user

You may wish to migrate a Regular user to an Active Directory user; this user will then be managed by your Active Directory. The user can now use Windows Authentication to access the intranet. They are no longer bound by Forms authentication only.

### Convert a Regular user to an Active Directory user

1.Create an Active Directory account for the desired user on your Domain. The account must have the first and last name fields filled out at a minimum.

2.If you are using AD integration and the automatic user creation feature, then be sure to add the AD account to the AD security group that ThoughtFarmer syncs with. This is configured on the Employee Directory Connector page.

3.Go to the ThoughtFarmer **Administration Panel**: **Users & security** section &gt; **User management** page.

4.Use the filter, sort, and query tools to find the desired user \(see [Find users ](../find-users.md)for more info\).

5.Click the gear icon in the **Action** column to the right of the user, and click **Edit account** in the menu that opens.

![](../../../.gitbook/assets/1%20%28108%29.png)



6.Select the radio button "Active Directory user".

7.Select the appropriate Active Directory from the **Active Directory configuration** dropdown menu.

8.Enter the AD username with the Domain in the provided text field. The format should be DOMAIN\username.

1. Click **Save.**

