# Password management for Active Directory users



### Password management for Active Directory users <a id="pageTitle_en"></a>

In order for Active Directory users to be able to change their passwords you first need to have Active Directory integration enabled on the Active Directory page.

### Enabling password changes for Active Directory users

1.Go to the ThoughtFarmer **Admin panel: Users & security** section &gt; **Employee Directory Connector** page.

2.Click on the **Active Directory** for which you want to enable password changes.

3.Click on the **Configuration** tab.

4.In the **User authentication** section, select the checkbox **Allow password changes**. In the box that appears, enter the number of days \(or leave the default number of days\) before the password expiry date that users will be warned to change their password.

5.Click **Save changes** at the bottom.

 A warning message will show on the user's homepage to remind them to change their password before it expires.  
  
When AD users change their password through ThoughtFarmer the old password may still be cached and usable for up to 15 minutes. Please see [http://support.microsoft.com/kb/267568](http://support.microsoft.com/kb/267568) for more info.

