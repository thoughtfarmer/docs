# System Logs

## System logs

The ThoughtFarmer **System logs** in the **Logs & statistics** section of the Administration Panel will show you detailed information on what is happening with both the web application and the ThoughtFarmer service. There are 4 different types of messages available:  
  
![6.7Admin8802Info.png](https://community.thoughtfarmer.com/imagethumb/53555170000/16564/600x600/False/6.7Admin8802Info.png) **Info**: Informational messages indicate general activity of various application processes. They indicate that things are working as expected. Typical informational messages are for index and activity updates when content is created/edited, AD synchronization tasks beginning, progress, and completion, etc.  
  
![](https://community.thoughtfarmer.com/imagethumb/169111900000/16563/300x300/False/sign_warning.png)  **Warning**: Warnings indicate that something did not work as expected. These types of messages are usually transient and should only be reported to ThoughtFarmer Support if a particular warning is happening consistently or the warning is being presented to the user during a certain action.  
  
![6.7Admin8802Error.png](https://community.thoughtfarmer.com/imagethumb/54080170000/16565/600x600/False/6.7Admin8802Error.png) **Errors**: Errors indicate that something that should have completed did not complete. The severity of errors ranges with the type of action that was trying to complete. These could be minor problems, such as an email notification error when a user does not have an email address filled in. These could be more severe problems if there is a configuration, network, or hardware problem that is preventing a particular application function. If you are seeing repeated or serious errors please report them to [ThoughtFarmer Support](http://helpdesk.thoughtfarmer.com/).  
  
![6.7Admin8802Debug.png](https://community.thoughtfarmer.com/imagethumb/56107670000/16566/600x600/False/6.7Admin8802Debug.png) **Debug**: Debug messages are special system log messages that are only logged when the site is in Debug mode. This is a very verbose logging mechanism. Typically, Debug mode should not be enabled unless you have been directed to do so by ThoughtFarmer Support. Debug mode is not performance optimized.

The Debug mode on/off toggle can be found on the **Admin panel**: **Logs & statistics** section &gt; **System logs** page.  
  
In addition to the System Logs in the ThoughtFarmer Administration Panel, all log messages are also recorded to the Application log on the web server. These messages will be shown in the Event Viewer from the source "Enterprise Library Logging".

## Configure filter

You can filter the current log view by the logging level, the day, and by specifying terms that the log message includes or excludes. Once you have chosen or entered your filters, click **Find**.  
  
**System log filter options:**

![](../../.gitbook/assets/3%20%2815%29.jpg)

You may also filter to a single error message ID. Users that receive error messages will also be given an error message ID. Please use this information when you create a ticket at [http://helpdesk.thoughtfarmer.com](http://helpdesk.thoughtfarmer.com/). Select the radio button "Filter by system log entry Id", enter the value, and click **Find**.

## Disable logging

The System Log will always be enabled by default. It is not recommended that you disable logging. If any problems arise the system log is the first stop for information concerning possible causes. If there is a problem that is causing you to consider disabling logging please contact [ThoughtFarmer Support](http://helpdesk.thoughtfarmer.com/).

