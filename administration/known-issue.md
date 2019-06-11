# Known issue

### Known Issues:

* [AV software and the ThoughtFarmer indexing service](known-issue.md)
* [AV software and notifications from ThoughtFarmer](known-issue.md)
* [Microsoft error reporting](known-issue.md)
* [Outlook error messages when syncing with ThoughtFarmer calendars](known-issue.md)
* [Desktop Connector connection issues over SSL](known-issue.md)
* [Malformed characters when using "Email this page"](known-issue.md)
* [Drag and Drop when attaching files](known-issue.md)

### AV software and the ThoughtFarmer indexing service <a id="section1"></a>

Antivirus software running on the same web server as ThoughtFarmer may cause conflicts. Symptoms of this issue are problems with tag display, site search, missing employee directory and groups listings.  
  
The conflict is caused when ThoughtFarmer creates temporary files while it is reindexing content. If the Anti-virus software is set to auto-scan new files, it may try to scan \(and lock\) these temporary files. The lock on the file will then prevent the indexer from moving or deleting the files which results in a corrupted index.

The following options will resolve this issue:

1. Disable auto-scanning of newly created files.
2. Disable scanning of all files in the **\_index**, and **\_resizedimages** folders. By default, these folders are located in the **c:\&lt;intranet name&gt;** folder, and can be confirmed by viewing **Administration Panel**: **Search** section &gt; **Search Index** page as well as the **Administration panel**: **Advanced options** section &gt; **System Caches** admin page.
3. Uninstall the antivirus service.

### AV software and notifications from ThoughtFarmer <a id="section2"></a>

In addition to problems caused by file scanning, some Antivirus software products prevent email related activity deemed to be malicious that is in fact benign. For example, if a change is made to a page that requires notifications to many people, ThoughtFarmer will send email to each user. Some anti-virus software will interpret this as an e-mail worm and block access to the SMTP server, preventing the message from being sent.

The following options will resolve this issue:

1. Disable outgoing SMTP scanning.
2. Uninstall the antivirus service.

### Microsoft error reporting <a id="section3"></a>

The error reporting service should be configured to exclude monitoring of the ThoughtFarmer application. This is because the ThoughtFarmer logging is very robust and logs errors that are not application critical. The error reporting service consumes a lot of resources if there are many errors to report. This can leave the CPU pegged for some time and leave the server in a crippled state. Error reporting is configured in Control Panel --&gt; System --&gt; Advanced --&gt; Error Reporting.

### Outlook error messages when syncing with ThoughtFarmer calendars <a id="section5"></a>

When you open a ThoughtFarmer calendar in Microsoft Outlook, users may get a string of errors. These error messages have been an ongoing issue with Outlook and its support for the iCal specification. Floating times are the way of having cross-time zone events automatically changed to a local user's time when importing. Outlook says it does not support floating time except for all-day events. Yet, when it imports it it still handles it correctly by converting the time to the local user's \(by assuming UTC\) but still throws multiple instances of the following error anyway:

> _Task "My Calendar" reported error \(0x00040023\) : 'The VEVENT, "My Event", defined near line 125, contains a floating DTSTART. Outlook supports floating time for all-day events only. Double-click to open this item._

  
This error message can be safely ignored without any adverse affects on the Calendar's functionality from within Outlook.

### Desktop Connector connection issues over SSL <a id="section6"></a>

If you are trying to connect the Desktop Connector to your ThoughtFarmer intranet over SSL then you will have authentication issues if there is an invalid certificate or self signed certificate. The Desktop Connector requires a valid SSL certificate to work properly.

### Malformed characters when using "Email this page" <a id="section7"></a>

Users working in a language that contains special characters may experience a malformed auto-generated email when clicking "Email this page" from within ThoughtFarmer. To fix this the users' mail client needs to be configured to allow for UTF-8 for the mailto protocol.  
  
In Outlook this can be changed by going to Tools --&gt; Options --&gt; Mail Format --&gt; International Options and then enabling UTF-8 support for mailto: protocol.

### Drag and Drop when attaching files <a id="section8"></a>

In ThoughtFarmer 8 the drag and drop functionality is supported in IE Edge, IE11, Chrome, FireFox and Safari. It is no longer support is IE9 or lower

