# ThoughtFarmer Service

### ThoughtFarmer Service

ThoughtFarmer 8.5 Services is a Windows service application that runs alongside your ThoughtFarmer website. The role of the service is to perform actions that can be run in the background, and automated tasks that do not require user interaction. Such tasks include: index updates, AD sync tasks, cache invalidation, incoming email parsing, outgoing email notifications, etc.  
  
ThoughtFarmer 8.0 EDC \(Employee Directory Connector\) Service also runs alongside your ThoughtFarmer website and performs actions related to authentication and syncing.  
  
**Go to**:

* [Web to service interaction via the Message Queue](thoughtfarmer-service.md)
* [Troubleshooting ThoughtFarmer Service issues](thoughtfarmer-service.md)
* [Restarting a stalled or failed service](thoughtfarmer-service.md)

###  Web to service interaction via the Message Queue <a id="section1"></a>

Certain user actions will trigger a message to be queued by the web application to be processed by the service. For example, when a user updates a page, the web application performs the work of updating the content in the database. It then queues messages for the service to process to notify watchers of that page, as well as to update the search index.  
  
All current messages waiting to be processed are visible in the **Message queue** screen under the **Advanced options** section of the **Administration panel**. This screen is divided into two sections: The **Global** **Queue** and the **Local Queue**.

Possible load balanced and replicated environments can vary greatly. Please consult [support@thoughtfarmer.com](mailto:support@thoughtfarmer.com) if you are considering an alternative architecture. 

### Troubleshooting ThoughtFarmer Service issues <a id="section2"></a>

If the ThoughtFarmer Service fails, stalls, or otherwise ends up in a corrupt state you may get reports of the following symptoms:

* Users do not receive notifications of changed, or new content.
* Emails sent to ThoughtFarmer are not being picked up.
* New pages added are not showing up in search results or on news/blog/forum pages.
* Active Directory synchronization tasks \(both scheduled and on-demand\) are not happening.

If issues like these arise, or even before they are reported, you may also see a message in the Administration Panel:  
![](https://community.thoughtfarmer.com/imagethumb/22563530000/16404/1000x1000/False/StaleMessages.png)  
  
You can check the state of the service by logging onto the web server and going to **Start** &gt; **Administrative Tools** &gt; **Services**. There will be an entry for the ThoughtFarmer Service with an indicator if it is started or not. If it is running then check the number of messages on the **Message queue** screen in the Administration Panel. Check the highest value for "Time in Queue". Certain service tasks such as indexing the portal, rebuilding extracted text, and any AD sync tasks may take up to 1 hour to perform. If a task takes much longer than an hour this is a cause for concern.  
 

### Restarting a stalled or failed service <a id="section3"></a>

Default installation configuration sets the ThoughtFarmer Service to restart itself if it fails. So a restart should only be necessary on a stall, or if configuration has been changed.  
  
Before actually restarting the service you may want to consider cleaning out the message queues first. This is a recommended first step if:

* It has been many days since the Service stopped working.
* There are 1000s of messages in the queue.
* There are repeated "IndexPortal" messages.

Cleaning out the queues first in this case will prevent notification spam to your users \(they will otherwise get a flood of notifications for the period the service was out\). It will also prevent it from immediately getting bogged down or performing tasks which only need to occur once.

####  Restart ThoughtFarmer Service without queue cleanup:

1. From the web server go to **Start** &gt; **Administrative Tools** &gt; **Services**.
2. Select the proper ThoughtFarmer Service from the list.
3. Select "Restart the service" or "Start the service" depending on what is available.
4. Go to **Administration panel**: **Advanced options** section &gt; **Message Queue** page to ensure messages are being processed. You should see messages disappear with each refresh.

####  Restart ThoughtFarmer Service with queue cleanup first:

1. From SQL Management Studio run the following query on the ThoughtFarmer database:

   > delete from localmessagequeue where localmessagetype &lt;&gt; 17  
   > delete from globalmessagequeue

2. From the web server go to **Start** &gt; **Administrative Tools** &gt; **Services**.
3. Select the proper ThoughtFarmer Service from the list.
4. Select "Restart the service" or "Start the service" depending on what is available.
5. Go to the ThoughtFarmer **Administration panel**: **Search** section &gt; **Search** **Index** page.
6. Select **Rebuild Search Index**.
7. Go to **Administration panel**: **Advanced options** section &gt; **System Caches** page.
8. Under **Object Caching** select **Flush cached data.**
9. Go to **Administration panel**: **Advanced options** section &gt; **Message Queue** page to ensure messages are being processed. You should see messages disappear with each refresh.

Once complete the web application and service should be up-to-date with each other again.  
  
If you think that you have a problem with the ThoughtFarmer 8.0 Services or the ThoughtFarmer 8.0 EDC Service and are unsure how to troubleshoot or correct it we recommend that you contact [support@thoughtfarmer.com](mailto:support@thoughtfarmer.com) so our support team can help diagnose and rectify the issue.

