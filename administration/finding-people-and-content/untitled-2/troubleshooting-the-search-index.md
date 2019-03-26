# Troubleshooting the search index



### Troubleshooting the search index <a id="section4"></a>

If you are having problems with the ThoughtFarmer search index, check the **Symptom** section below. If you are experiencing one or more of these symptoms on your intranet, follow the corresponding solution to resolve the problem.  
  
**Symptom:** 

* No results are displayed on search results pages
* Search results are incomplete or greatly inaccurate
* No results are displayed within the People Directory
* People or security groups are not populating Security or Following dialogs

  
**Problem:**   
The index has become corrupt or out of date. This may occur due to one or several of the following reasons:

* The ThoughtFarmer Windows Service is off.
* Indexing errors \(e.g. index name is incorrect or missing\)
* Elastic Search settings have been misconfigured
* Index files are being locked by anti-virus software

  
**Solution:**

1. **​**Check that the ThoughtFarmer Windows Service is running on the application server. If it is **OFF** then proceed to step 1.1. If it is **ON** then proceed to step 2.
   1. Check the message queue via the **Administration panel**: **Advanced options** section &gt; **Message queue** page to see how long the ThoughtFarmer Windows Service has been off for. If it has been off for an extended period of time \(for example 10 days\) clear the queue out by clicking the **Purge all current tasks** button. This ensures that when the service is turned back on users don't get outdated notifications and alerts. 
   2. Once you have purged the tasks go to the application server and turn the ThoughtFarmer Windows Service back on.
2. Check the system logs to verify if any errors are occurring.
3. Contact the ThoughtFarmer Helpdesk to verify your Elastic Search configuration or check for any anti-virus issues you think may be occurring.

