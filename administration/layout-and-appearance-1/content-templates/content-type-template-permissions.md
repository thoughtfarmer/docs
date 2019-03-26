# Content type template permissions

### Who can edit templates?

Administrators can make changes to templates on the **Administration panel: User interface** section &gt; **Content type templates** page. When an administrator makes changes to a template using that Admin page, all pages that use that template are affected, unless they have been modified on the individual page level.  
  
Only users who have been granted special content type template permissions by the administrator are able to modify templates on individual pages. When a user has permission to do this, they will see a **Modify template** option at the top left of the template in the Update Cards window in Edit mode. Clicking **Modify template** allows the user to add and remove Cards from the page, and to reorder or change the column placement of Cards. To learn more, see[ How to modify templates](../../../using-thoughtfarmer/add-pages-and-sections/modify-templates.md).  


![](../../../.gitbook/assets/2%20%288%29.jpg)

### Change template editing permissions

To control who has permission to customize templates for individual pages:

1. Go to the **Administration panel: Users & Security** section &gt; **Content type template permissions** page.
2. Select the radio button beside the group to which you want to give permission to modify individual page templates:

   i.Administrators only

   ii.Everyone who has View and Edit permission on a page

   iii.Members of the security profile that you select \(if they have edit permission on a page\). For this option, select the radio button and then click on **Select a security profile**, and select the desired security profile from the menu that opens.

3. Click **Save changes**.

### Modified page type templates

Administrators can view which pages have had their templates modified. To do this, go to the page **Administration panel: User interface** section &gt; **Content type templates** page, and click on **In use** below a template to see a list of pages that use that template.  


![](../../../.gitbook/assets/3%20%2821%29.jpg)

There are two tabs at the top of the list - Default and Modified. The Default tab shows pages that use the template as is. The Modified tab shows pages that have had the template modified on the individual page level.

![](../../../.gitbook/assets/4%20%2840%29.jpg)



Click on the **Modified** tab at the top to see pages with modified templates. Modified template pages will not be affected if the content type template they were based on is edited by an administrator on the Admin Content type templates page.

### Learn more:

* [How to modify page templates](create-and-modify-template/)
* [How to modify templates in edit mode](../../../using-thoughtfarmer/add-pages-and-sections/modify-templates.md)
* [How to create a security profile](../../security/security-groups.md)

