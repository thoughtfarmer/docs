# Profile details

### Profile details

The Profile details admin page allows administrators to determine what information can be added when a user edits their profile. Administrators determine what profile fields display, what fields are required, what fields contribute to profile strength, and whether any fields can only be edited by administrators.

### Profile Strength indicator

At the top of the Profile details admin page is a checkbox option regarding the Profile Strength indicator. The Profile Strength indicator shows on profile pages only to the profile owner and to admins, and also shows when editing your profile. The Profile Strength indicator only displays when strength is less than 100%. Essentially, the more information a user adds to their profile, the stronger their profile strength. To learn more, see [Profile Strength](profile-strength.md).

### **Show Shout-outs on profile**

At the top of the Profile details admin page is a checkbox option to Show Shout-outs on profile pages. If selected, the number of Shout-outs a user has received shows below their name on their profile page. Clicking on the number of Shout-outs displays a list of the Shout-outs in a pop-up window. To learn more see [Shout-outs settings & reports](../../customize-your-content/shout-out-settings-and-reports.md).

![](../../../.gitbook/assets/5%20%2830%29.png)

### Profile completeness report

Near the top of the Profile details admin page, there is a button called **Download profiles \(.csv\)**. Clicking this button will download a file that contains profile information for all active users, sorted alphabetically by last name. Administrators can use the report to see who has filled out their profile, how much they have filled out, and the content of each profile field.

![](../../../.gitbook/assets/6%20%2813%29.png)

Each profile field is listed in a separate column. If the Show profile strength indicator option is selected on the Profile Details page, then the Profile strength column indicates the percentage of profile strength for the user. The Profile photo column indicates whether the user has uploaded a profile photo or not. Private and password custom fields are not displayed in the report.

### Profile sections

By default there are four sections on the Profile details admin page. The sections found here determine what sections are available when users edit their profiles, and what sections show on profile pages. The four default sections are: Featured information, Contact & Bio, Relationships & Groups, and Expertise & Skills. Featured information shows in the headers of profile pages, and the other sections appear as tabs on profile pages.  
  
Each of the sections contains multiple information fields that users can fill out. There are default fields in each section, and administrators can add additional fields.

### Add new section

Administrators can add new sections to the profile details page, which will show as new tabs on profile pages. To add an information field to an existing tab, see the Add new field section.

1. Go to the **Administration panel**: **Content** section &gt; **Profile details** page.
2. Click the **Add Section** button at the bottom of the page. The **New section** pop-up window appears.
3. Click in the text box and type a **title** for the section. If multiple languages are enabled on your intranet, click in the other language boxes and type titles for them.
4. Click **Save** in the **New section** window.

See the Add new field heading below to add fields to your newly created section.

### Add new field

Add a field to a section to add another place for users to add a specific piece of information on their profile. Field content is added to the search index, so any values populated will be searchable to help find specific users. There are eight types of fields that can be added. The tag type of field also allows for filtering of users into any desired set of criterion by using tag facets for search.​

1. Go to the **Administration panel**: **Content** section &gt; **Profile details** page.
2. Find the section that you want to add the field to.
3. Click **Add field** under that section. The **New field** pop-up window appears.
4. Select the type of field that you want to create. \(See Field types heading below for descriptions of the field types.\)
5. Click in the **Field label** box and enter a name for the field. \(If multiple languages are enabled, add a name for each language in the corresponding text box.\)
6. Options:
   1. Check the **Display field** box to have the field display for users \(the option to hide the field is not present for all fields\).
   2. Check the **Make this field required** box to require users to fill out the field.
   3. Check the **Only allow editing by administrators** box to prevent users from entering info in the field.
   4. Check the **Count towards profile strength** if you want this field to add to the profile strength in edit profile.
7. Enter additional information as required for the Dropdown list or Tags field types. \(See Field types heading below.\)
8. Click **Save** in the **Edit field** window.

### Field types <a id="section1"></a>

There are 8 types of  fields that can be added:

* **Text**: A single line of text
* **Text \(Private\):** This is the same as a text field, except it cannot be seen by any other users except the profile owner. These fields are intended for use in custom Cards.
* **Text Area**: A multi-line text area
* **Rich Text Editor**: A multi-line text area with the full editor in place for formatting
* **Dropdown List**: A customizable dropdown list for user selection. You must add items for the dropdown list when you create this type of field. Click in the Display Text box and type the dropdown list item. Click in the Value box to enter a unique value or ID that corresponds to the dropdown item and is used when syncing with external user management services. Click **Add another dropdown option** to add more dropdown items.
* **Tags**: A tag area that allows multiple additional terms to be added. These tags can be used to filter and find ThoughtFarmer users. This field type is used as part of the [Expertise locator](../untitled-4/) feature of ThoughtFarmer. If you wish, add or select tags that will be recommended to users for that field by typing them in the **Add tags** box, and then either selecting the tag or choosing to create a new tag in the dropdown menu. If tag creation for users is enabled on your intranet, users will be able to add their own tags to this type of field. To learn more about enabling tag creation, see [Tagging overview](../untitled-5/tags-overview.md).
* **Password \(Private\)**: This is the same as a private text field, except the characters are masked in the input field, and the value is stored in the database using encryption. These fields are intended for use in custom Cards.
* **Link**: Allows the user to choose a link from the intranet, an external website, or an email address.
* **Date**: Allows the user to select a date from a calendar.

Any fields \(with the exception of tags\) can be mapped with any field in a user's Active Directory account.

Profile fields that are added are not displayed on the Employee Directory by default. To learn about customizing the Employee Directory listings, see [Employee directory format](../untitled-3.md).  

### Other actions

**Reorder fields**: Drag and drop fields to reorder them within sections or switch them to a different section.  
**Reorder sections**: Drag and drop sections to reorder them.  
**Change the field label:** Click the **gear icon** beside the field, type a new label in the window that appears and click **Save**. If you have multiple languages enabled, be sure to update the labels for all languages.  
**Hide field**: Click the gear icon beside the field and uncheck the **Display field** box in the **Edit field** window. Fields can be hidden even if users have already filled them out. The information will be saved but will not appear on their profile. New users will not see hidden profile fields.  
**Delete field**: Click the garbage can icon beside the field and then click **Delete** in the window that appears to confirm the deletion. Information that users have entered in the field will be lost if you delete the field. Not all fields can be deleted, but they can be hidden instead.  
**Delete section**: Click the garbage can icon beside the section and then click **Delete** in the window that appears to confirm the deletion. A section can only be deleted if there are no fields in it.

### Mapping Fields with Active Directory <a id="section4"></a>

Any field can be mapped to any attribute within a user's Active Directory account. To allow this, Active Directory integration needs to be configured and enabled. To learn more, see [Active Directory Field Mappings](../../activity-directory-integration/active-directory-field-mappings/). If a field is mapped to Active Directory or another external user management service, the checkbox **Only allow editing by administrators** should be selected so that users cannot edit the field.  
 

### Tip: Change user settings

Administrators can change certain user settings on a user's profile page. To do this, go to the **user's profile page**, click the **down arrow** on the right of the of the **Page Controls**, and click **Settings** in the options that appear. An administrator can then change settings about timezone, archiving, alternate email and notifications for that user.

