# Embedding reports

If you want to make a ThoughtFarmer Analytics widget available in an external applicaiton, such as your ThoughtFarmer intranet, you are able to do so. Any widget in ThoughtFarmer Analytics can be embedded and will function exactly as it does if you were logged into the dashboard itself. This is a great way to share reports directly with others without requiring them to obtain their own ThoughtFarmer Analytics accounts or login.

### **To embed a report**

1. Click on **Administration** \(cork icon\) on the top right of the ThoughtFarmer Analytics site.
2. Select **Platform** from the left hand side menu and click **Widgets**.
3. Select the **date range** desired for the report \(using the Date Range picker\).
4. Under **Widgetize** reports section, choose the report category by hovering your cursor on the category.
5.  A pop up with the preview of the widgetized report will be displayed.
6. Copy the **Embed iFrame** code from below the preview window.

```text
<iframe 
src="https://analytics.thoughtfarmer.com/index.php?module=Widgetize&action=iframe&moduleToWidgetize=Dashboard&actionToWidgetize=index&idSite=3&period=week&date=yesterday"; frameborder="0" marginheight="0" marginwidth="0" width="100%" height="100%">
</iframe>
```

Once you have the embed code there is one final step required to embed this. In order for the report to be anonymous and accessible without login a token auth parameter must be added to the iframe src parameter. To do this, you can grab the token parameter directly from the API link at the top of the Intranet Statistics page. The parameter will be highlighted there and be copied in whole. It will look like the following:

```text
&token_auth=e5cb856a7abcdef38ca43fd6638bb1ed
```

Take that value and paste it at the end of the src attribute in the iFrame embed code. The final result \(example below\) can now be added to any ThoughtFarmer page using the **Insert Code** tool, or directly by switching to the **Source** view. You can also embed this on any web page on an external site. 

```text
<div id="widgetIframe">
<iframe width="100%" height="350" 
src="https://analytics.thoughtfarmer.com/index.php?module=Widgetize&action=iframe&widget=1&moduleToWidgetize=VisitTime&actionToWidgetize=getVisitInformationPerServerTime&idSite=3&period=month&date=2019-01-09&disableLink=1&widget=1"; 
scrolling="no" frameborder="0" marginheight="0" marginwidth="0">
</iframe>
</div>
```

