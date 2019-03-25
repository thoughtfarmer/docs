# Add custom content to header

### How to add custom content to header

Some clients add navigation elements to the right of their logo in the header. To do this go to the **Administration panel** &gt; **User interface** section &gt; **Theme** page.  
  
Add the content you need, in HTML format, to **Theme** page &gt; **Custom HTML** tab &gt; **Custom header HTML**.  
Add any needed link references to **Theme** page &gt; **Custom HTML** tab &gt; **Custom &lt;HEAD&gt; tag content**.  
Add any needed script references to **Theme** page &gt; **Custom HTML** tab **&gt; Custom footer HTML**.  
  
Here is a sample that adds 4 navigation links to the header:

### Custom header HTML

```text
<div id="system-links">
    <a href="http://cat">Cat</a>
    <a href="http://infrared/">Infrared</a>
    <a href="http://rhythm/">Rhythm</a>
    <a href="http://tribe">Tribe</a>
</div>
```

### Custom &lt;HEAD&gt; tag Content

As an example, this area can be used to add custom fonts to your ThoughtFarmer instance. Below is the link reference for the custom fonts that you would add to this section. See[ Add custom web fonts](../../add-custom-web-fonts.md) for full instructions on adding custom fonts to your ThoughtFarmer instance.

```text
<link href='http://fonts.googleapis.com/css?family=Skranji:400,700|Gabriela' rel='stylesheet' type='text/css'> 
```

### Custom footer HTML

The extra footer area is where you would put any script references that are required to customize your ThoughtFarmer instance.  
  
For example  
  
&lt;script type = "text/javascript"&gt;  
  
&lt;/script&gt;

