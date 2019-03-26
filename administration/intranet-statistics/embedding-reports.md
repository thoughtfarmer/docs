# Embedding reports



If you want to make an Intranet Statistics widget available in an external applicaiton, such as your ThoughtFarmer intranet, you are able to do so. Any widget in Piwik can be embedded and will function exactly as it does if you were logged into Piwik itself. This is a great way to share reports directly with others without requiring them to obtain their own Piwik accounts or login.  
  
![Embedded+widget.png](https://community.thoughtfarmer.com/imagethumb/181613600000/16392/498x308/False/Embedded+widget.png)  
  
**To embed a report:**

1. Click on **Widgets** in the top of the Piwik site.
2. Select the date range desired for the report \(using the Date Range picker\).
3. Choose the report category.
4. Choose the exact report. This will display a preview of the report on the page.
5. Copy the **Embed iFrame** code from below the preview window.

  
  
Once you have the embed code there is only one final step required to embed this. In order for the report to be anonymous and accessible without login a token auth parameter must be added to the iframe src parameter. To do this you can just grab the token parameter directly from the API link at the top of the Intranet Statistics page. The parameter will be highlighted there and be copied in whole. It will look like the following:  


```text
&token_auth=e5cb856a7abcdef38ca43fd6638bb1ed
```

Simply take that value and paste it to the end of the src attribute in the iFrame embed code. The final result \(example below\) can now be added to any ThoughtFarmer page using the **Insert Code** tool, or directly by switching to the **Source** view. You can also embed this on any web page on an external site.   


```text
<div id="widgetIframe"><iframe width="100%" height="350" src="http://stats.thoughtfarmer.com/index.php
?module=Widgetize&action=iframe&moduleToWidgetize=ThoughtFarmer
&actionToWidgetize=getUserActivity&idSite=10471&period=day
&date=2012-11-17&disableLink=1&widget=1&token_auth=e5cb856a7abcdef38ca43fd6638bb1ed" 
scrolling="no" frameborder="0" marginheight="0" marginwidth="0"></iframe></div>
```

