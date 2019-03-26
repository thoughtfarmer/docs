# Alternate error message for no view permission

When a user clicks a link they will see the 404 - Not Found error message if the linked-to page has been deleted, or if they do not have permission to view the page.

![](../../../.gitbook/assets/1%20%2824%29.jpg)

Admins can choose to have a different message show if the page exists but the user does not have permission to view the page. The default alternate message is:

![](../../../.gitbook/assets/2%20%2856%29.jpg)



To control whether Error 404 or an alternate message shows when a user does not have permission to view a page:

1. Go to the **Administration panel**: **Advanced options** section &gt; **Configuration settings** page.
2. Type **security** in the **Search config settings** field to narrow the config settings results.
3. Find the config setting security.showForbiddenPage.
4. Click in the **Value** column beside the config setting.
   * Select the **false** radio button to show Error 404 for pages where a user does not have permission to view.
   * Select the **true** radio button to show an alternate message for pages where a user does not have permission to view.
5. Click **Save**.

  
Admins can change two labels to customize the alternate message. In the image above it shows what parts of the message the labels correspond to. To change the alternate message:

1. Go to the **Administration panel**: **User interface** section &gt; **Labels** page.
2. Under the **Label** heading, click in the dropdown menu and find the label **ErrorForbiddenTitle**.
3. Under the **New Label Value** heading, click in the text box and type the new message title.
4. Click **Add**.
5. Under the **Label** heading, click in the dropdown menu and find the label **ErrorForbiddenMessage**.
6. Under the **New Label Value** heading, click in the text box and type the new message body.
7. Click **Add**.
8. Now your alternate message will show if **true** has been selected for the config setting security.showForbiddenPage.

