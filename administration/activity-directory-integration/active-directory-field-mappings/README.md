# Active Directory field mappings



### Active Directory field mappings

ThoughtFarmer user profile fields can be mapped to Active Directory account attributes. Depending on the settings you choose, this means that when information changes in one of the Active Directory or a ThoughtFarmer profile, it is automatically updated in the other.  
  
Each profile is matched to a person's name, so the minimum requirement for Active Directory integration is to map the _First name_ and _Last name_ ThoughtFarmer fields \(_givenName_ and _sn_ in Active Directory\).  
  
ThoughtFarmer can also sync any custom profile field with any Active Directory user attribute. Once you have [created the custom field](../../finding-people-and-content/untitled-7/) in ThoughtFarmer it will be available in the dropdown when creating a new field mapping in Active Directory.  
  
**Go to:**

* [Choose the data owner for a mapped field](./)
* [Create a new field mapping](./)
* [Edit an existing field mapping](./)
* [Delete an existing field mapping](./)
* [Default ThoughtFarmer fields to Active Directory attributes](./)

### Choosing the data owner for a mapped field <a id="section1"></a>

The data owner can be set to either ThoughtFarmer or AD on a field by field basis. For ThoughtFarmer to be the data owner of any fields, AD write access needs to be enabled on the specific Active Directory page, and the AD service account needs write permissions to AD user attributes. If ThoughtFarmer is the owner of a mapped field then any changes made on a user's profile will overwrite that value in AD when the profile changes are saved.  
  
With AD as the data owner, any changes users make to their profile fields within ThoughtFarmer are overwritten by the AD values whenever the [synchronization task](../active-directory-synchronization-tasks.md) Bulk update users occurs. Because of this you may wish to [make fields with AD as the data owner non-editable by users.](make-profile-fields-non-editable.md)  
  
An example of field mappings and data owner settings is shown at the bottom of the page.

### Create a new field mapping <a id="section2"></a>

1.Go to the ThoughtFarmer **Administration Panel**: **Users & security** section &gt; **Employee directory connector** page.

2.Click on the **Active Directory name** for which you want to create a new field mapping.

3.Click on the **Field Mappings** tab.

![](../../../.gitbook/assets/1%20%2878%29.jpg)



4.Click **Add** at the bottom.

5.Select the **ThoughtFarmer field** from the dropdown.

6.Enter the case sensitive AD attribute in the **External store field**.

7.Select **ThoughtFarmer** or **AD** as the **Data owner** in the dropdown.

8.Click the **Save** icon on the right of the field mapping.

Note: The "External store field" column is free-text and case sensitive. If you are unsure of the exact attribute name in AD you can use [AD Explorer](http://technet.microsoft.com/en-us/sysinternals/bb963907.aspx) to get the specific Active Directory user attributes available on your system.

### Edit an existing field mapping

1. Go to the ThoughtFarmer **Administration Panel**: **Users & security** section &gt; **Employee directory connector** page.
2. Click on the **Active Directory name** for which you want to edit a field mapping.
3. Click on the **Field Mappings** tab.
4. Click the **edit icon** \(a pencil\) beside the field mapping that you want to edit.

![](../../../.gitbook/assets/3.jpg)

5.Change the desired values

5.Click the **Save icon**.

### Delete an existing field mapping

1. Go to the ThoughtFarmer **Administration Panel**: **Users & security** section &gt; **Employee directory connector** page.
2. Click on the **Active Directory name** for which you want to delete a field mapping.
3. Click on the **Field Mappings** tab.
4. Click the **garbage can icon** beside the field mapping you want to delete.

### Example ThoughtFarmer fields to Active Directory attributes

The following is a list that shows an example of ThoughtFarmer profile fields and their usual mapping to Active Directory user attributes. This is just a guide. Fields can be mapped to any AD attribute you wish.

| ThoughtFarmer field | Active Directory attribute | Data owner \(ThoughtFarmer or AD\) |
| :--- | :--- | :--- |
| First name | givenName | ThoughtFarmer |
| Last name | sn | ThoughtFarmer |
| Email | mail | Active Directory |
| Title | title | ThoughtFarmer |
| Telephone | telephoneNumber | ThoughtFarmer |
| Mobile | mobile | ThoughtFarmer |
| Fax | facsimileTelephoneNumber | ThoughtFarmer |
| UserAddressLine1 | streetAddress | ThoughtFarmer |
| UserAddressLine2 | l | ThoughtFarmer |
| UserAddressLine3 | st | ThoughtFarmer |
| UserAddressLine4 | postalCode | ThoughtFarmer |

