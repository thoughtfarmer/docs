# Password management for Regular users



### Password management features available for Regular users

* **Regular users can always change their own passwords:** On their profile page, users can click the down arrow on the right of the page header to open the Page Controls and find the **Change password** link.

![](../../../.gitbook/assets/1%20%2829%29.png)

* **Regular users can reset their own password if they forget it:** The forms login page has a **Forgot password** link that Regular users can use should they forget their passwords. This will send them an email with a link that allows them to reset the password. There is no need for administrator intervention.

![](../../../.gitbook/assets/2%20%2827%29.png)

**Note:** Regular user passwords will never expire. 

### Strong password policy

Strong passwords are enabled by default for Regular users. This means that administrators and users can only set passwords that meet the minimum strong password requirements. All strong passwords must contain the following:

* at least 8 characters
* at least one lowercase letter
* at least one number or special character
* at least one uppercase letter

### Change strong password policy for Regular users

1. Go to the **Administration panel**: **Authentication** section &gt; **Regular user settings** page.
2. Under **Strong passwords** set the checkbox "Require strong passwords for regular users" to the desired value.

![](../../../.gitbook/assets/3%20%2814%29.png)



1.Click **Save changes** at the bottom.

To view the strong password policies, click **View the strong password policies** on the Regular user settings page.

### Password lockout

You can configure the password lockout for failed password attempts. This will lockout any Regular user account for a specified period of time after a configured number of failed tries.

### **Configure password lockout for Regular users**

1.Go to the **Administration panel**: **Authentication** section &gt; **Regular user settings** page.

2.Under **Password security**, fill out the desired values X and Y for "Password attempts before lockout \[X\] and a lockout duration of \[Y\] minutes."

![](../../../.gitbook/assets/4%20%2810%29.png)

3.Click **Save changes** at the bottom.

