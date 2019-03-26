# Attachement settings

### Attachment settings

Upload and download restrictions for attachments can be set based on file type. Using this feature can restrict potentially malicious or unwanted file types from being uploaded. You can also restrict certain file types from being displayed in the browser on download. The attachment settings for both uploads and downloads can be found on the **Administration panel**: **Content** section &gt; **Files and images** page.

### Upload options <a id="section1"></a>

The **Uploading** section on the **Files and images** page has two fields available for entry. The **Allow all** list is a blacklist that will restrict _only_ those file types that are specified. The **Only allow** is a whitelist that will restrict all attachments from being uploaded _except_ those specified. Choose the list type that is most appropriate for your restriction scheme by selecting the radio button beside it. Then enter the list of file extensions in a comma-separated list.  
  
The following shows the ThoughtFarmer default values for the upload attachment settings:  
![5.5+Admin+6112+Upload+settings.png](https://community.thoughtfarmer.com/imagethumb/155349200000/16736/1000x1000/False/5.5+Admin+6112+Upload+settings.png)

Note: If you change the list to exclude files that have previously been uploaded, they will no longer appear.

###  Display attachments in-browser <a id="section2"></a>

The download attachment settings will dictate which file types can be automatically displayed in the browser \(where applicable\). By restricting a file type from being displayed you can force the download action to prompt the user to choose a program to open the file, or save the file to disk. The two fields here work the same way they do in the upload settings \(above\). The **Allow all** is a blacklist, and the **Only display** is a whitelist. Choose whichever is appropriate and enter a comma-separated list of file types.

The ThoughtFarmer default settings \(shown below\) restrict the most common file types that are associated with [Cross Site Scripting \(XSS\)](http://en.wikipedia.org/wiki/Cross-site_scripting) attacks.  
![5.5+Admin+6112+Download+attachment+settings.png](https://community.thoughtfarmer.com/imagethumb/155525600000/16737/1000x1000/False/5.5+Admin+6112+Download+attachment+settings.png)

Note: Some file types must be downloaded and saved locally before viewing regardless of the download settings in ThoughtFarmer.

