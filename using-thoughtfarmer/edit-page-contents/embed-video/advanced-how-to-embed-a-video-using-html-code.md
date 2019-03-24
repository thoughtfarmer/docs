# Advanced:How to embed a video using HTML code



The preferred method is to use ThoughtFarmer's built-in embedding options or use an external Video service. This method should only be used if you must use a file format that is not in the list of supported file types \(see [Video formats and conversion](video-formats-and-conversion.md)\) OR you are on a version prior to 8.0.1.25. This method requires working with HTML directly. So if you are not comfortable with coding then be sure to contact a colleague who is.  
  
Please see the page on [Video formats and conversion](video-formats-and-conversion.md). Even if you are using this method it is recommended you use **MP4** using **H.264** encoding for the greatest browser and device support on the web.

**Disadvantages:**

* Requires manual modification of HTML.
* Does NOT support HTTP streaming, only progressive download. This means your users will not be able to skip forward in a video until that portion of the video has downloaded. The built-in method supports skipping ahead on-demand.

**Upload files to the server**

It is highly recommended that you upload video files to the server for use with this method. There is a Virtual directory called **Extensions** that is available specifically for hosting assets and add-ons to the application. If you do not have access to the server, get your IT to upload your files there, or contact ThoughtFarmer supportif you are on Cloud. All files once uploaded can be referenced from ThoughtFarmer using https://yourintranet.com/extensions/video.wmv. You can visit that URL directly to verify the video has been uploaded correctly.   
  
You can use the download URL for a file attached to an actual ThoughtFarmer page for this method. However, please note that it will not be cached \(viewing the file again triggers a fresh download\), and places heavier load on the application.   
 

**Create HTML Video tag**

Use the following template as a guide:

```text
<video controls="" height="240" width="320">
  <source src="/extensions/myVideo.mp4" type="video/mp4" />
Your browser does not support the video tag.
</video>

```

  
The colored portions above represent areas that you will need to edit manually. 

* The green areas show the height and width of the video. 
* The blue src parameter must be changed to match the source URL of the location of the video. 
* The red type will correspond to the extension of the video. Just look up the mime-type by extension.
*  The orange control attribute is optional and can be tailored to suit the needs of the player. See [W3 Schools](http://www.w3schools.com/html/html5_video.asp)for basic info and options, and [Mozilla Developer Network](https://developer.mozilla.org/en/docs/Web/HTML/Element/video) for advanced options. 

  
Once you have modified the HTML embed code all you need to do is:

1. **Edit the destination page**: On the page you wish to embed the video click the **Edit button** \(pencil icon\) in the page header. Move your cursor to the location where you wish the video to show. Use the **Insert code** ![5.5%2BUser%2B5928%2BInsert%2Bcode%2Bbutton%2B2.png](https://community.thoughtfarmer.com/imagethumb/130633270000/15966/950x950/False/5.5%2BUser%2B5928%2BInsert%2Bcode%2Bbutton%2B2.png)button and paste the embed code in the pop-up window. Click the **Insert** button in the pop-up window. 
2. Click **Save**. The video will now show on the page.

