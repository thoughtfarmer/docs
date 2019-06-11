# Guest users



### Guest users

You can allow guest users to access your ThoughtFarmer intranet. Guest users view the intranet in Read-only mode, and therefore are unable to edit content or add comments. They do not have profiles and do not count toward your ThoughtFarmer license seats. The ability of guest users to view and download content is managed by the [security profile "Guests"](../security/security-groups.md).  
  
All users of your ThoughtFarmer intranet must be authenticated. Guest users must have a valid network account \(either AD or local\). This is not the same as true anonymous access.

### **Enable guest users**

Guest access must be enabled for each login provider individually. 

1.Go to the **Administration panel** &gt; **Authentication** section &gt; **Login provider** page.

2.Click on the **name** of the **login provider** you want to enable guest users for. This will allow you to edit the login provider settings.

3.In the **Form/Windows/Custom SAML configuration** section, under **Guest access**, select the radio button for the desired level of Guest access.

![](../../.gitbook/assets/1%20%2872%29.jpg)

4.Click **Save**.

5.Repeat **steps 2 to 4** to enable guest access for other login providers.

### Guest user criterion

* A guest user account must have an active Active Directory or External user account.
* A guest user must not have an active profile created for them in ThoughtFarmer.
* If Active Directory syncing and automatic user creation are enabled, then the user must not be a member of the synced with Active Directory security group configured on the Employee Directory Connector page.

