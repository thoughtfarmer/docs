# Configure tags for the Expertise Locator

### Configure tags for the Expertise Locator

Tags for the Expertise Locator are specific to people, and so are grouped into their own bundles, separate from content tag bundles. Since these bundles are tied to custom profile fields they are configured on the [Profile Details Admin page](../untitled-7/) instead of the Tags Admin page. However, the list of profile field tags and profile field bundles can be viewed on the Tags admin page, and profile field tags can be added, merged and deleted from there as well. To learn about merging and deleting tags, see [Manage tags](../untitled-5/manage-tags.md).

### Create tags in user profile custom fields <a id="section1"></a>

Tag custom fields must be added to existing profile sections. Profile sections show up as separate tabs or sections when viewing or editing profile pages. These profile sections are also shown on the Employee Directory to organize the tags associated with users. To learn how to add profile sections, see [Profile details](https://community.thoughtfarmer.com/content/105971).

### Add new tag type field with tags

Add a tag type field to a profile section so users can add tags that will help other people find them with the Expertise Locator. Field content is added to the search index, so any values populated will be searchable to help find specific users. A field must be Tag type to work for the Expertise Locator. Once you have completed these instructions, users will be able to edit their profile and select tags to add information to a section of their profile.  
  
**Custom profile section and field as seen on the Profile Details Admin page:**

![](../../../.gitbook/assets/5%20%2842%29.png)



1.Go to the **Admin panel**: **Users & security** section &gt; **Profile details** page.

2.Find or create the profile section that you want to add the field to. See [Profile details](../untitled-7/) to learn how to add profile sections.

3.Click **+ Field** under that section. The **New field** pop-up window appears.

4.Select the **Tags** type of field.

5.Click in the **Field label** box and enter a name for the field. \(If multiple languages are enabled, add a name for each language in the corresponding text box.\)

6.Options:

1. Check the **Display field** box to have the field display for users.
2. Check the **Make this field required** box to require users to fill out the field.
3. Check the **Only allow editing by administrators** box to prevent users from entering info in the field.
4. Check the **Count towards profile strength** if you want this field to add to the profile strength in edit profile.

7.To add tags:

1. Click in the **Add tags** box.
2. Type a tag name in the field. If the tag already exists, click on it in the dropdown menu. If the tag does not exist, click the **Create new tag** option in the dropdown menu. Tags you have added will show below the Add tags box.
3. Repeat step 2 to add more tags.

8.Click **Save** in the **New field** window.

9.Click **Save** at the bottom of the page.

**Custom profile section and field as seen on a user profile page:**

![](../../../.gitbook/assets/6%20%2829%29.png)

### Free tagging and custom profile field tags <a id="section2"></a>

Free tagging can be enabled through the [Tags page](../../../using-thoughtfarmer/tags/) in the Administration panel. This configuration option has an effect on both regular and custom profile field tags. With free tagging enabled users are able to create tags on the fly. If a user enters a value that is not an existing tag in that specific custom field, then they are given the option to create it, as shown below.

![](../../../.gitbook/assets/7%20%2820%29.png)

When a user creates a tag in a custom profile field, the tag will be added to that profile field bundle. In the above image, the newly created tag "Rugby" will now be part of the profile field tag bundle "Sports". Tags created by users on other content on the intranet is added to the generic group **Unbundled tags**.  
  
With free tagging _disabled_, users cannot add any new tags. They will instead only be able to choose tags that have been added to a specific custom field by an administrator.

