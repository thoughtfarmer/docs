# Filter content

### Content Filters <a id="section2"></a>

These are content filters created by ThoughtFarmer. Content filters are only applied once a page is saved.

#### Change the content filters

1. Go to the **Administration panel**: **Advanced Options** section &gt; **Configuration Settings** page.
2. Type **rich** in the **Search config settings** field to narrow the list of config settings.![5.5Admin6117ConfigureRTE2.png](https://community.thoughtfarmer.com/imagethumb/148394200000/3565/1000x1000/False/5.5Admin6117ConfigureRTE2.png)
3. Search for the config setting richTextEditor.customContentFilters.
4. Click in the **Value** column, and enter a comma-separated list of filters.
5. Click **Save**.

**After changing the configuration setting, restart the application pool in order to apply the changes.**

**System filters**: FixObjectTags, ConvertImageAttributesToSrcParameters, ConvertUrlsToAnchors, ConvertEmailsToMailTos. These filters are used internally by ThoughtFarmer to perform basic content cleanup tasks. These filters should not be removed.  
  
**Enhanced security filter set**: ConvertImageAttributesToSrcParameters, FixObjectTags, ConvertUrlsToAnchors, StripHtmlComments, StripHtmlStyleTags, ConvertEmailsToMailTos, ScrubHtml  
  
**Allow javascript filter set**: any combination _not_ including DefaultFilters, ScrubHtml, or StripHtmlScriptTags.

| Filter Name | Description |
| :--- | :--- |
| FixObjectTags \(system\) | Tidy up object tags to make sure that they have a wmode attribute |
| ConvertImageAttributesToSrcParameters \(system\) | This is an internal filter used to manage the properties of images uploaded into ThoughtFarmer, it should not be removed from the list of applied filters |
| ConvertUrlsToAnchors \(system\) | Find URLs within the content and convert them to a clickable link in the content |
| ConvertEmailsToMailTos \(system\) | Find email addresses within the content and convert them to mailto: links |
| ScrubHtml | Removes all tags and attributes from the content that could be used for malicious actions. This is to help prevent cross site scripting attacks \(XSS\) |
| StripHtmlComments | Find all Html comments within the content and remove them |
| StripHtmlScriptTags | Find all Html script tags within the content and remove them |
| StripHtmlStyleTags | Find all Html style tags within the content and remove them |
| DefaultFilters | ConvertUrlsToAnchors \| ConvertEmailsToMailTos \| ConvertDisplayNameToProfileLin k \| StripHtmlComments |

