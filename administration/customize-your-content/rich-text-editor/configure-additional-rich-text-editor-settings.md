# Configure additional Rich Text Editor settings

### Configure additional Rich Text Editor settings

To change the following configuration settings:

1. Go to the **Administration panel**: **Advanced options** section &gt; **Configuration settings** page.
2. Type **rich** in the **Search config settings** field to narrow the list of config settings.

   ![5.5Admin6117ConfigureRTE2.png](https://community.thoughtfarmer.com/imagethumb/148394200000/16494/349x32/False/5.5Admin6117ConfigureRTE2.png)

3. Find the config setting that you want to change in the **Name** column.
4. Click in the **Value** column beside the config setting, and change the current value.
5. Click **Save.**

#### Configure inserted image height and width

Default image insertion height and width \(in pixels\) can be adjusted using the config settings richTextEditor.insertedImageHeight and richTextEditor.insertedImageWidth.

#### Configure enter key behavior

The "Enter" key can be configured to insert a new line break when the config setting richTextEditor.newLineBr is set to true. When false, the "Enter" key will insert a new paragraph with a non-breaking space.

#### Add custom CSS file to editor content

You can add custom CSS files to the content area of the editor. To do this, use the richTextEditor.custom.css config setting. Add paths, relative or absolute, to custom CSS files, separated by a comma.

#### Turn off spell check

Chrome, Firefox, Safari, and some versions of Internet Explorer have a built-in spell check. If your organization primarily uses Chrome, Firefox or Safari, turn off ThoughtFarmer's internal spell check and take advantage of the built-in browser spell check. To do this, use the config setting richTextEditor.native.spellcheck.enabled, and set the value to True. For end user information, see the page [Rich Text Editor and spell check.](../../../using-thoughtfarmer/edit-page-contents/rich-text-editor-and-spell-check.md)

#### Select fonts and font colors available in RTE

To learn more, see [Specify available fonts and font colors.](../../advanced-configuration/configuration-settings/specify-available-font-and-font-colors-in-rte.md)

#### Enable in-page linking

When the config setting richTextEditor.inPageContentLinksEnabled is set to True, a new icon appears to the right of the Insert link/Unlink icons that allows users to create link target IDs in the page. Users can then create links in the page that will link to the place/heading they have set as a link target.  


