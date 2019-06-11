# Terms and conditions



### Terms and conditions

Certain legal protocols in your organization may require that users accept a set of terms and conditions before accessing the intranet. You may also wish to present a disclaimer to users. Both of these can be configured from the **Administration panel**: **Content** section &gt; **Terms & conditions** page.  
  
Terms and conditions configured from within ThoughtFarmer will be shown to your users once on first login. They will be presented with the declared Terms & Conditions statement and asked to accept or decline. They will only proceed to ThoughtFarmer if the terms are accepted. You can change the terms & conditions at anytime and trigger a reset so users will be able to review the new terms the next time they log in.

### Configure a disclaimer

A disclaimer can be added to your ThoughtFarmer intranet. This is simply any additional information or content that you want users to be aware of at all times. The disclaimer is shown on all profile pages in the footer.

1.Go to the ThoughtFarmer **Administration panel**: **Content** section &gt; **Terms & conditions** page.

2.Ensure that the feature is enabled in the status section. If not enabled, click **enable**.

![7.1Admin10588EnableTerms.jpg](https://community.thoughtfarmer.com/imagethumb/40831800000/16578/950x950/False/7.1Admin10588EnableTerms.jpg)

3.Enter content into the **Disclaimer** rich text area.

![](../../.gitbook/assets/1%20%2864%29.png)



4.Click **Save settings** at the bottom.

Configure terms and conditions

1.Go to the ThoughtFarmer **Administration panel**: **Content** section &gt; **Terms & conditions** page.

2.Ensure that the feature is enabled in the status section. If not enabled, click **enable**.

![](../../.gitbook/assets/2%20%2864%29.jpg)

3.Enter content into the **Terms & conditions of use** rich text area.

![](../../.gitbook/assets/3%20%288%29.png)

4.Enter a rejection URL into **Terms and conditions of use rejection URL**. This is where users will be redirected if they decline the terms.

![](../../.gitbook/assets/4%20%2858%29.png)

1. Click **Save settings** at the bottom.

If you have not enabled terms & conditions previously then the above steps will trigger all users to accept the new terms.

### Update terms and conditions <a id="section2"></a>

If you do not require all your existing users to accept the updated terms then do not click **Reset terms and conditions** in step 2 below. In that case only new users will be shown the updated terms. A copy of the latest accepted terms by each user is stored individually; so at any time there is a record of the exact version a particular user accepted.

1. Configure the new Terms & conditions of use as shown in the steps above.
2. Click **Reset terms and conditions**.

![](../../.gitbook/assets/5%20%2819%29.png)

3.Click **Save settings**.

### Configure an alternate acceptance URL <a id="section3"></a>

By default all users will be redirected to the homepage when they accept the terms. You may wish instead to redirect them to a specific page on your intranet, such as a welcome announcement, or new user help page.

1.Go to the ThoughtFarmer **Administration panel**: **Advanced options** section &gt; **Configuration settings**page.

2.Type **terms** in the **Search config settings** field to narrow the list of config settings.

![](../../.gitbook/assets/6%20%2830%29.png)

3.Find the config setting termsAndConditions.acceptUrl.

4.Click in the **Value** column beside the config setting and enter the address for the ThoughtFarmer page. It is recommended to use relative addressing \(e.g. "/content/3125"\).

5.Click **Save**.

