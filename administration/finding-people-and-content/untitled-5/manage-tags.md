# Manage tags

### Manage tags to refine searches

Any ThoughtFarmer administrator can organize tags and tag bundles. The **Tags** page in the **Administration panel** allows you to add, delete and merge content and profile field tags. You can also add and delete tag bundles and organize all tags into bundles. The Tags page also provides you with usage counts for existing tags on pages and on ThoughtFarmer profile custom fields.  
  
See [Manage tag bundles](manage-tag-bundles.md) for more information about tag bundles.  
  
There are a few ways to create tags. You can add them to the general list of all Content Tags or you can add them to a specific Tag Bundle or Profile Field when you create them. With [tag creation enabled](tags-overview.md), all users can add new tags to pages at any time. These will all be grouped in "Unbundled tags".

### Find tags

There may be hundreds of tags on the intranet, but admins can use Filter and Sort features on the Admin Tags page to find the tags they are looking for in either the Content Tags or Profile Field Tags tab.

![](../../../.gitbook/assets/1%20%2889%29.png)

On the left of the Admin Tags page, you can enter a **search query** into the **Search tags** box to narrow the list of tags. You can also select certain **filters** to narrow down the list, depending what tab you are viewing.  
  
Filters available under the **Content Tags** tab:

* **Tag name**: the number or letter the tag starts with
* **Bundle**: which tag bundle the tag belongs to
* **Type**: the type of page the tag is attached to
* **Usage count**: how many times the tag has been used

Filters available under the **Profile Field Tags** tab:

* **Tag name**: the number or letter the tag starts with
* **People**: the person whose profile the tags are attached to
* **Usage count**: how many times the tag has been used
* **Profile field**: what profile field the tag belongs to

Search queries or selected search filters will appear above the filtered list of tags and can be removed by clicking the X beside the query or filter, or clicking Clear filters to remove all filters.  
  
To **sort** the list of tags, click on one of the headings at the top of list of tags. **Content Tag/Profile Field Tag**sorts the list alphabetically by tag \(A-Z or Z-A, with numbers preceding letters\). **Usage** sorts tags from most to least used or least to most used. **Bundle** sorts tags alphabetically by the bundle they belong to, also grouping Unbundled tags together. **Profile Field** sorts tags alphabetically by the profile field they belong to.  
  
Clicking on the Usage number beside a tag will take you to a search results list showing all of the content that has that tag attached to it. Clicking on the bundle name beside a tag will take you to a bundle page that shows all of the tags in that bundle, and allows you to add, remove, merge or delete tags in that bundle. To learn more, see [Manage tag bundles.](manage-tag-bundles.md)

### Create tags

#### Create tags by adding them to the full list of tags

This method adds content tags created to "Unbundled tags". If you use this method and you want the tags to be in a bundle, you will need to manually add the tags to specific tag bundles.

1.Go to the ThoughtFarmer **Administration panel**: **Content** section &gt; **Tags** page.

2.Under the **Content Tags** tab, click **Add Tag**.

![](../../../.gitbook/assets/2%20%2893%29.png)

3.Type the value for the new tag in the text area that appears and click the **checkmark** to save the tag.

1. If the tag already exists, you will see a message appear "A content tag with this label already exists".

#### Create tags by adding them to a specific bundle

Add content tags directly to an existing bundle using these instructions.

1. Go to the ThoughtFarmer **Administration panel**: **Content** section &gt; **Tags** page.
2. Click on the **Content** **Bundles** tab.
3. Click on **the existing tags** beside the bundle you want to add to, or click on the **... menu** on the right of the bundle and click **Manage Bundle** in the menu that appears.

![](../../../.gitbook/assets/3%20%2840%29.png)

4.Click **Add Tag**.

![](../../../.gitbook/assets/4%20%2825%29.png)

5.Type the value for the new tag in the text area that appears and click the **checkmark** to save the tag. The tag will appear in the list of tags for that bundle.

![](../../../.gitbook/assets/5%20%288%29.png)



#### Create profile field tags by adding them to a specific profile field

1. Go to the ThoughtFarmer **Administration panel**: **Content** section &gt; **Tags** page.
2. Click on the **Profile Field Tags** tab.
3. Click on the **Profile Field** you want to add a profile field tag to.
4. Click **Add Tag**.
5. Type the value for the new tag in the text area that appears and click the **checkmark** to save the tag. The tag will appear in the list of tags for that profile field.

To learn more about profile field tags and how they are used, see [Expertise locator](../untitled-4/).

### Merge tags

An administrator may want to merge tags with similar meanings, or tags that are simply variations on a word, into one tag. Especially when all users are allowed to create tags, tags with similar meanings may be created on the intranet.  
  
After tags are merged, content that previously used any of the tags that were merged will be tagged with the one tag that was selected to merge into. Merged content tags will join the bundle of the tag they are merged into. Profile field tags must be in the same profile field in order to be merged. Note that you can only merge tags under the same tab, you cannot merge Content Tags and Profile Field Tags.

1.Go to the ThoughtFarmer **Administration panel**: **Content** section &gt; **Tags** page.

2.Under the **Content Tags** or **Profile Field Tags** tab, select the checkboxes beside the tags that you want to merge. \(Note that you can only merge tags under the same tab, you cannot merge Content Tags and Profile Field Tags.\)

3.Click **Merge tags**. \(The Merge tags button will only appear after multiple tags are selected.\)

4.In the **Merge tags** window, click on the tag that you want to merge the tags into. \(If the tags selected are profile field tags, the profile field that they belong to will also show in the window.\)

![](../../../.gitbook/assets/6%20%287%29.png)

![](../../../.gitbook/assets/7%20%2816%29.png)

5.Click **Save**. The tag list will be updated showing the new usage for the merged tag.

### Delete tags <a id="section4"></a>

Tags can be deleted from the Content Tags tab or the Profile Field Tags tab using this method.

1.Go to the ThoughtFarmer **Administration panel**: **Content** section &gt; **Tags** page.

2.Scroll through the list of tags or use the Search and Filter tags area on the left to find the tag you want.

3.Select the checkbox to the left of the tag.

![](../../../.gitbook/assets/8%20%2812%29.png)

4.Repeat steps 2 and 3 to select multiple tags. The selected tags will show in a list at the top of the tab.

![](../../../.gitbook/assets/9%20%2812%29.png)

5.Click **Delete**.

6.Click **Confirm** in the **Delete tags** dialog ****to confirm the deletion.

All deleted tags will be removed from all associated tag bundles and content.

