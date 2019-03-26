# Wufoo forms integration



### Access Wufoo forms on your intranet

Wufoo integration allows intranet users to be able to add [Wufoo](http://www.wufoo.com/) forms to intranet pages. A specific Wufoo account is integrated with the intranet so that forms created under that account are accessible for embedding on intranet pages. The ability to add forms to intranet pages can be allowed for all users or restricted to administrators only.  
  
For user instructions about adding Wufoo forms, see [How to add a Wufoo form](../../using-thoughtfarmer/edit-page-contents/embed-forms-widgets-and-more/add-wufoo-forms.md).

### Enable Wufoo integration

1. Go to the **Administration Panel**: **Content** section &gt; **Wufoo integration** page.
2. Click **enable**.![6.7Admin9149EnableWufoo2.png](https://community.thoughtfarmer.com/imagethumb/37449400000/16408/600x600/False/6.7Admin9149EnableWufoo2.png)
3. In the **Wufoo subdomain** field, enter the subdomain you use to access your Wufoo account. \(eg. if you access your Wufoo account at http://acme.wufoo.com, your subdomain is acme.\)

![](../../.gitbook/assets/1%20%2846%29.png)



4.In the **Wufoo API token** field, enter your Wufoo API key. For more information, see [Finding your key.](http://help.wufoo.com/articles/en_US/SurveyMonkeyArticleType/Wufoo-REST-API-V3#Findingthekey)

5.If you want only administrators to be able to add Wufoo forms, select the checkbox "Only administrators may embed wufoo forms".

6.Click **Test settings**. The **Verify Wufoo integration settings** dialog will appear.

7.Click **Verify**.

1. If the test fails to connect to your Wufoo subdomain \(you see a red X icon![6.7Admin9149WufooTestFails.png](https://community.thoughtfarmer.com/imagethumb/36132830000/16407/600x600/False/6.7Admin9149WufooTestFails.png)\), double-check that you have entered your subdomain and Wufoo API token information correctly, and test the settings again.
2. If the test succeeds, you will see a green checkmark and a message indicating the successful connection. Close the dialog and continue.

![](../../.gitbook/assets/2%20%2863%29.png)

8.Click **Save changes**.

### Remove the ScrubHtml filter to allow Wufoo integration

In order for users to successfully add Wufoo forms on intranet pages, the Rich Text Editor filter ScrubHtml must be disabled. Follow the steps below to do this:

1. Go to the **Administration panel**: **Advanced options** section &gt; **Configuration settings** page.
2. Type **rich** in the **Search config settings** field to narrow the config settings results.![6.7Admin9149RemoveFilter2.png](https://community.thoughtfarmer.com/imagethumb/46813300000/16410/600x600/False/6.7Admin9149RemoveFilter2.png)
3. Find the config setting richTextEditor.customContentFilters.
4. Click in the **Value** column beside the config setting. It will say **DefaultFilters,ScrubHtml**.
5. Delete the **ScrubHtml** filter.
6. Click **Save**.
7. Recycle the application pool on the web server.

