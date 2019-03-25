# insert UNC file link



### Using UNC file links

You may have a file that you want to be accessible from your ThoughtFarmer intranet, but that you don't want to upload to your intranet. UNC file links allow you to link directly from the intranet to files on your network. Depending on the link source and browser settings, when a user clicks on a UNC file link, it may download the file, open it in a browser tab, or direct the user to a folder.  
  
UNC file links will only work within your network. The URL of the intranet must be in the trusted sites or local intranet zone of the IE browser in order for these links to work.  
  
Users must be accessing the intranet using Intranet Explorer for UNC file links to work. These links will not open in any other browser as they are blocked for security reasons.  
  
The link must be in the following format: [file://servername/foldername/file.txt](file://servername/foldername/file.txt).

### How to create UNC file links

1.Go into edit mode on the page where you want to create the link.

2.Click on the **Insert link** button in the Rich Text Editor.

![](../../../.gitbook/assets/1%20%28116%29.jpg)

3.The **Insert link** pop-up window will open. Click on the **External location** tab on the left.

![](../../../.gitbook/assets/2%20%2811%29.png)



4.In the **Location** box at the top, type the source of your file. It must be in the format [file://servername/foldername/file.txt](file://servername/foldername/file.txt). When you type you will see the **Link To** path at the bottom of the window start to form with file:// at the beginning.

5.If you wish the link to show in text other than the Link To path, type the text you want in the **Link Label** box.

6.Click **Insert** and **Save** the page.

