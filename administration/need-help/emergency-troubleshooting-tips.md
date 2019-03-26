# Emergency Troubleshooting Tips

From time to time you may encounter problems with your ThoughtFarmer intranet that you don't know how to resolve. This guide lists some scenarios that you may encounter, and contains instructions on how to troubleshoot these problems. If you don't find the appropriate solution below, please contact the [ThoughtFarmer Helpdesk](http://helpdesk.thoughtfarmer.com/) for assistance.

### Scenario 1: A 404 or 503 service unavailable message is seen

When this message appears it will mean that either your IIS site or application pool is turned off. You can rectify with the following steps

1. Access the server that runs your ThoughtFarmer intranet, or contact someone who can. 
2. Proceed to IIS. This will be listed under the administrative tools.
3. Check that the IIS site is turned on. If its off you will see a little stop symbol over the site name.
4. Click on application pools in IIS and check that the application pool for the site is on. If its off you will see the little stopped symbol over the application pool name.

Once you have confirmed that both of these are started try and access the site again

### Scenario 2: No one is able to access the intranet

**For Active Directory users**

1. Check the database to see if all users have been set to inactive. If users are inactive, check Active Directory to ensure all users are active. If they are not, set all users to Active.
   1. This can be done by querying the database with 'select \* from \[user\] where isactive = 1'. This will search for all inactive users
2. Activate at least one user through the database so they can access the intranet to troubleshoot further.

Query to perform this action:UPDATE \[user\]Set isactive = 1  
where userid = \[place userid you want to activate here, excluding brackets\]

1. Once the query has been executed, recycle the application pool so the change will take effect.
2. Once a user can access the intranet, proceed to the **Administration Panel**: **Users & Security** section &gt; **Employee Directory Connector** page in order to run a sync with Active Directory to activate all other users.

**For all users**

1. Check the event viewer on the web server under "application logs".
2. Check for messages related to SQL server, eg.
   1. Connection to SQL server lost
   2. Invalid credentials to connect to SQL server.

### Scenario 3: A specific user is unable to access the intranet

#### For Active Directory Users

If the user receives an "access denied" message or is logged in as a guest member then check the following areas:

**If automatic user creation is turned on**

1. Check if the affected user is in the Active Directory group that you are syncing with ThoughtFarmer. The sync group is listed on the **Administration panel**: **Users & security** section &gt; **Employee Directory Connector** page for the Active Directory.
2. If the user **is not** in the Active Directory group:
   1. Add the user to the group and then sync ThoughtFarmer with Active Directory. To sync, go to the **Administration Panel**: **Users & Security** section &gt; **Employee Directory connector** page, and click on the appropriate Active Directory. At the bottom of the page are the **On-Demand synchronization** options. Run the **Refresh user lookup list** and **Bulk create users** synchronizations.
   2. Check if the user can log in.
3. If the user **is** in the Active Directory group:
   1. Check if the user has a profile on ThoughtFarmer. It is possible the user has two profiles due to a name change in Active Directory.
   2. If the user has two profiles, delete the new profile and follow the [steps to take when a user changes their name](https://thoughtfarmer.zendesk.com/entries/21989618-Steps-to-take-when-a-user-changes-their-name).
4. If the user still has problems logging in, it is possible that the correct credentials are not being passed through the system due to multiple accounts being created. Perform a restart of the web server.

**If automatic user creation is turned off**

1. Ensure that a profile has been created for the specific user before the user attempts to log in.

### **Scenario 3: Editing a page gives errors**

1. Go to the **Administration panel**: **Authentication** section &gt; **Active Directory** page and click on the appropriate Active Directory.
2. In the **Active Directory settings** section, click **change**.
3. Ensure no messages appear stating that credentials are invalid. If a message exists stating that the credentials are invalid, determine the correct credentials and re-enter them into the settings area.
4. Recycle the application pool on the web server if performance is poor.

### Scenario 4: Search / Employee directory is down

1. Rebuild the index for the site:
   1. Navigate to the **Administration panel**: **Search** section &gt; **Search settings** page and click **Rebuild index -&gt; Rebuild index now -&gt; Delete index before rebuild**
   2. Check the system logs \(**Administration panel**: **Logs & statistics** section &gt; **System logs** page\) for the message stating that the index has been rebuilt. \(This will take some time depending on the amount of content you have on your intranet.\). You will also be able to see the status from the search index settings screen.
   3. Once the index has been rebuilt check the affected Employee directory / Search directory again.
2. Check if there is virus protection software on the server.
   1. If virus software exists, create an exception for the ThoughtFarmer folder that contains the index and resized image folder.

If the issue persists ensure that the exception for the virus software was made correctly.  
  
If you need further assistance with the problem you are experiencing, please feel free to contact the [ThoughtFarmer Helpdesk](https://community.thoughtfarmer.com/external?url=http%3A%2F%2Fhelpdesk.thoughtfarmer.com).

### Useful troubleshooting documentation

* [Active Directory synchronization tasks](../activity-directory-integration/active-directory-synchronization-tasks.md)
* [Active Directory basic settings](../activity-directory-integration/active-directory-basic-settings/)
* [Steps to take when a user changes their name](https://community.thoughtfarmer.com/content/13607)
* [Search Index](../finding-people-and-content/untitled-2/)
* [System Logs](../behind-the-scenes/system-logs.md)

