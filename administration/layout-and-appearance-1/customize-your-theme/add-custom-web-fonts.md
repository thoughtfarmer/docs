# Add custom web fonts

### Add custom web fonts using the Theme page

In ThoughtFarmer there are many default fonts available out of the box but you may also want to apply custom web fonts to your intranet. This is a fairly simple process. The steps below use Google Web Fonts as an example.  
  
There are 2 main areas in ThoughtFarmer where you need to make changes in order for your web fonts to appear. These two areas are:

* The **Custom &lt;HEAD&gt; tag content** area on the **Administration panel** &gt; **User interface** section &gt; **Theme**page.
* The theme.fontfamilies configuration setting in the **Administration panel** &gt; **Advanced options** section &gt; **Configuration settings** page.

### Adding the font to the "Custom &lt;HEAD&gt; tag content area

1. Proceed to the [Google Web Fonts website](http://www.google.com/fonts/).
2. Choose a desired web font and then click **Add to Collection**.
3. At the bottom of the page click **Use**.
4. On the new page, choose the style of font that you want as well as the character sets. This page also includes all of the code that you need in order to apply the font to your ThoughtFarmer instance.
   * Please note that for this example we are going to apply the "Merriweather Sans" and "Gabriela" fonts to our ThoughtFarmer instance.
5. Copy the code in the **Add this code to your website** section and paste it in the **Custom &lt;HEAD&gt; tag content** area found on the **Administration panel** &gt; **User interface** section &gt; **Theme** page &gt; **Custom HTML** tab. Click **Save** at the bottom of the page.

Once this has been completed, follow the steps below to add the font family to the theme.fontfamilies configuration setting so that it will show up in the font dropdown.

### Adding the font family

1. Proceed to the **Administration panel** &gt; **Advanced options** section &gt; **Configuration settings** page.
2. In the **Search config settings** box, type theme.fontfamilies. The configuration setting will appear with all of the default fonts listed in the value field.
3. Copy the font\(s\) that are listed on the **Google Web Fonts** **page** under **Integrate the fonts into your CSS**and paste them into the **Value** field.
   * For our example we copy 'Merriweather Sans', sans-serif; and 'Gabriela', serif; into the area. Ensure that the fonts are separated by a semi-colon \(;\) in the configuration setting.
4. Click **Save** on the **Value** field.
5. Go to the **Administration panel** &gt; **User interface** section &gt; **Theme** page &gt; **Fonts and Headings** tab.
6. Select from the dropdown in order to apply the new font to your ThoughtFarmer intranet.
7. Click **Save** at the bottom of the page.

### For advanced users

You may only want to apply your custom font to certain areas of your ThoughtFarmer instance. For example, you may want all of the H1 headings in the site to use the custom font. To do this, add the following code to the CSS section of the **Theme** page:  
  
h1 { font-family: 'Metrophobic', Arial, serif; font-weight: 400; }  
  
This allows you to apply some fonts using the dropdown and others through this custom code.  


