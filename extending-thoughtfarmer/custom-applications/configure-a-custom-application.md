# Configure a custom application



### Configure a sub-application in IIS

To create a sub-application in IIS you must perform the following steps:

1. Logon to the server.
2. Deploy the sub-application files to a location on the server. \(e.g. _**C:\inetpub\ThoughtFarmer\{InstanceName}\ccadventureworks**_\)
3. Open the IIS administration tool.
4. Create a new application pool for the sub-application. Settings should match those supported for your sub-application type.
5. Select the site you wish to add the sub-application to.
6. Click "Add application".
7. Give the sub-application a name for it to be accessed through ThoughtFarmer.
   * For example, the name _**ccadventureworks**_ would be accessible through [https://yourintranet.com/ccadventureworks](https://yourintranet.com/ccadventureworks)
8. Select the application pool from step \#4.
9. Select the folder from step \#2.
10. Click **Ok.**

![](../../.gitbook/assets/5%20%282%29.png)

![](../../.gitbook/assets/6%20%2823%29.png)

### Configure an application in ThoughtFarmer <a id="configure"></a>

Once that is set up, go to the ThoughtFarmer **Administration panel** &gt; **User interface** section &gt; **Cards** page. Create either a **Global application** or **Page template application**, depending on your needs. These will function exactly like their global and page custom card counterparts.  
  
**Server url:**  
When the custom application loads either as a global card, or regular page card, this URL is called with a GET request. This URL must be accessible and configured as a sub-application. Query parameters are supported here and will be passed along with the call.  
  
**Javascript url:**  
This is the URL that the custom card will pull the JavaScript code from. This can be any custom JavaScript code and can utilize the ThoughtFarmer JavaScript API for custom card development. The result must be pure JavaScript. Jsx is not currently supported.   
  
**CSS url:**  
This is the URL that the custom card will pull a CSS style file from. Sass files are NOT currently supported at this time.  
  
**Configuration**:  
On the details tab you can enter default configuration for the card. If this is a page application then the option to "Allow card configuration on edit page" will be available. This functions exactly the same as the regular custom cards.

![](../../.gitbook/assets/7%20%2815%29.png)

