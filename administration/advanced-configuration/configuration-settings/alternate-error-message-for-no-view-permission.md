# Alternate error message for no view permission

When a user clicks a link they will see the 404 - Not Found error message if the linked-to page has been deleted, or if they do not have permission to view the page.

![](../../../.gitbook/assets/1%20%2824%29.jpg)

Admins can choose to have a different message show if the page exists but the user does not have permission to view the page. The default alternate message is:

![](../../../.gitbook/assets/2%20%2856%29.jpg)

To control whether Error 404 or an alternate message shows when a user does not have permission to view a page:

1. Go to the **Admin panel**: **Advanced** section &gt; **Configuration settings** page.
2. Type **security** in the **Search config settings** field to narrow the config settings results.
3. Find the config setting security.showForbiddenPage.
4. Click in the **Value** column beside the config setting.
   * Select the **false** radio button to show Error 404 for pages where a user does not have permission to view.
   * Select the **true** radio button to show an alternate message for pages where a user does not have permission to view.
5. Click **Save**.

  
Admins can change two labels to customize the alternate message. In the image above it shows what parts of the message the labels correspond to. To change the alternate message:

1. Go to the **Admin panel**: **User interface** section &gt; **Labels** page.
2. To make a new label override, click **Add label**. The Add label window will appear.
3. Select the language of the override from the dropdown \(only enabled languages will show here\).
4. Under **Resource file**, select the Common radio button.
5. Click in the **Label** search box and start typing **ErrorForbiddenTitle**. Select **ErrorForbiddenTitle** in the dropdown menu that appears.
6. Click in the **New Label Value** box, and type the new message title.
7. Click **Save**.
8. Repeat Steps 2 to 7 to change the value for the label **ErrorForbiddenMessage**.
9. Now your alternate message will show if **true** has been selected for the config setting **security.showForbiddenPage**.

To edit a label that has already been changed, hover over the existing entry and click the **pencil icon** beside the **New label value**. After editing the new label value, click the **checkmark** to save.

