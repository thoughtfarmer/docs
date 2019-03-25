# Active Directory basic settings

### Active Directory basic settings

If ThoughtFarmer will be integrated with multiple Active Directories, you will need to follow the instructions below for each Active Directory.

### **Active Directory service account**

In order for ThoughtFarmer to access an Active Directory it needs to use the credentials of an AD account that has the appropriate permissions. This is a service account that should **NOT** have a password expiry set. If there is a password expiry set, ThoughtFarmer authentication and other components may fail.  
  
To use all of the Active Directory integration features of ThoughtFarmer this account needs to have read and write access. For permission information please see [AD security permissions](active-directory-security-permissions.md). Please also see the page [Features requiring write access to Active Directory.  
](feature-requiring-write-access-to-active-directory.md)  
If you do not intend to use these features, or if your security protocols restrict this usage, then read-only access to AD is sufficient.

### Add new Active Directory <a id="section2"></a>

1. Go to the ThoughtFarmer **Administration panel**: **Users & security** section &gt; Employee directory connector page.
2. Click **Add new external user store**.
3. Type the Active Directory name in the **Name** box.
4. Select **Active Directory** in the **Type** box.
5. Select the checkbox **Enabled**.
6. Select the checkbox **Write enabled** if you want the user information in your ThoughtFarmer intranet to be able to write/override user information in your Active Directory \(see the Write Access heading below for more information.\)
7. Select the checkbox **User auto-creation** if you want users created in Active Directory to automatically have accounts created for them on your intranet.
8. Click **Save**. You will be taken to the configuration page for the Active Directory that you just created.

### Configure Active Directory integration <a id="section2"></a>

1. Go to the **Administration panel** &gt; **Users & security** section: Employee directory connector page, and click on the **Active Directory** that you want to configure. \(If you just followed the steps above to add a new Active Directory, you are already on the right page.\)
2. Click on the **Configuration** tab.
3. Enter your domain name in the **Domain** field.
4. Enter the AD service account name in the **Username** field. \(See above for details about the AD service account.\)
5. Enter the AD service account password in the **Password** field.
6. \(Optional\) Type any alternate domains in a comma separated list in the **Alternate domains** field. This is used for the login form only. Local machine and AD domain are included by default.
7. \(Optional\) Under **User authentication**, select the checkbox **Allow password changes**. Once selected, select the number of days \(before the password expiry date\) that users are warned to change their password in the **day warning period** box.
8. \(Optional\) Under **User authentication**, select the checkbox **Check user is still active** to enable TF to check if the user is still set as active in AD.
9. Under **Incoming mail domains**, enter the **Internet email domain** and the **LAN email domain**.
10. \(Optional\) Under **Properties**, enable LDAPS connection to Active Directory by selecting the **LDAPS** checkbox.
11. Under **Properties**, select the **Use ranged queries** checkbox. \(Almost all configurations will have this checkbox checked.\)
12. Under **Cross reference lookups**, the **Distinguished name lookup** and **NetBIOS name lookup** fields are highly specific to the customer environment, and are used mainly for troubleshooting when necessary. If you think you may need to use these fields, contact ThoughtFarmer Support.
13. Click **Save changes** at the bottom of the page.

### Write access <a id="section3"></a>

Enabling write access means that ThoughtFarmer can be the owner of various profile information fields. Information that is changed in ThoughtFarmer will update and overwrite information in Active Directory if write access is enabled and ThoughtFarmer is the Data owner for that particular field.  
  
If write access is disabled, no information in your Active Directory will be altered by ThoughtFarmer. Please see [Features requiring write access to Active Directory](feature-requiring-write-access-to-active-directory.md) for more information.  
  
To change the write access setting, go to the **Administration panel** &gt; **Users & security** section: Employee directory connector page, and click on the **Active Directory** that you want to change write access for.  
  
Under the **Basic Information** tab, check the **Write enabled** checkbox to enable write access. Uncheck the **Write enabled** checkbox to disable write access. Click Save**.**  


