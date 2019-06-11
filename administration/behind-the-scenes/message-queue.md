# Message queue

### Message queue

The **Message queue** screen is an informational screen and is used to aid in troubleshooting issues. To view the message queue screen go to the **Administration panel**: **Advanced options** section &gt; **Message queue** page.  
  
The message queue in ThoughtFarmer is used to execute actions outside of the normal requests for pages. Each message represents an action to be performed and the actions can include sending emails, indexing content for search, reading from/writing to active directory, retrieving RSS feeds, etc.  
  
The messages are processed by ThoughtFarmer 7.0 Services which is a Windows service application which is installed on the web server as part of the ThoughtFarmer installation process.  
  
Typically the message queue screen will be empty as the messages are processed as soon as they are added to the queue.  
  
If this page contains a long list of messages it can mean that either the ThoughtFarmer 7.0 Services application has been stopped, and is no longer processing the messages in the queue, or that there is a particular message that is taking a long time to be processed.  
  
Please see the [ThoughtFarmer Service](thoughtfarmer-service.md) page for troubleshooting issues with the Message queue. If you still have troubles please contact [http://helpdesk.thoughtfarmer.com](http://helpdesk.thoughtfarmer.com/).  


