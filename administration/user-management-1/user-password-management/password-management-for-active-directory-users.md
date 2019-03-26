# Password management for Active Directory users



### Password management for Active Directory users <a id="pageTitle_en"></a>

In order for Active Directory users to be able to change their passwords you first need to have Active Directory integration enabled on the Active Directory page.

### Enabling password changes for Active Directory users

1.Go to the ThoughtFarmer **Administration panel: Authentication** section &gt; **Active Directory**  page.

2.Click on the **Active Directory** for which you want to enable password changes.

3.In the Active Directory settings box, click **Change**.

4.In the User authentication settings section, under **Allow password changes** , select the checkbox "Allow password changes with a warning period of X days." \(X represents the number of days \(before the password expiry date\) that users are warned to change their password.\)

5.You can leave the number of days as the default number, or type a new number of days in the field.

![](../../../.gitbook/assets/1%20%2854%29.jpg)



6.Click **Save settings** at the bottom.

 A warning message will show on the user's homepage to remind them to change their password before it expires.  
  
When AD users change their password through ThoughtFarmer the old password may still be cached and usable for up to 15 minutes. Please see [http://support.microsoft.com/kb/267568](http://support.microsoft.com/kb/267568) for more info.

