# Configure Sharepoint Connector

### Configure the SharePoint Connector <a id="section3"></a>

Once the [SharePoint Connector setup](./) is complete, you are ready to enable and configure the SharePoint Connector from within ThoughtFarmer. Go to the **Administration Panel**: **SharePoint Connector** section &gt; **Settings**page. Click **enable** to turn the connection on and bring up the configuration page.

![](../../../.gitbook/assets/1%20%286%29.jpg)

There are 4 main sections to the configuration page:

#### **1.** SharePoint Connector features

![](../../../.gitbook/assets/2%20%2869%29.jpg)

Select the checkbox beside the desired feature\(s\) and click **Save changes** in order to make it available from within ThoughtFarmer:

> * **Linking enabled**: Use the ThoughtFarmer link browser to search and add links to SharePoint content.
> * **Document library integration enabled**: Users can add SharePoint document libraries to ThoughtFarmer pages via the Rich Text Editor. In order for document library integration to be successful, the Rich Text Editor filter scrubHtml cannot be enabled. See **Remove the ScrubHTML filter** below for complete instructions.
> * **Search integration enabled**: Search queries from ThoughtFarmer will occur in SharePoint as well and display the results of both.
> * **Office 2010 Web Applications integration enabled**: By adding the Office 2010 Web Application integration your users will have cross-browser editing capability of Office documents in document libraries embedded within ThoughtFarmer.
>
> Note: Please see SharePoint Integration Requirements for a list of technologies required for each feature listed above. Some require additional configuration steps from within SharePoint.

#### **2.** SharePoint servers

![](../../../.gitbook/assets/3%20%2830%29.jpg)

For each SharePoint server you wish to connect to ThoughtFarmer you need to add the required information to the SharePoint Servers section. You will need:

> * **Integration Service URL**: The URL along with the port the SharePoint Connector Service is running on \(e.g. http://sharepoint:8088\). From a firewall perspective, this URL needs to be accessible from the ThoughtFarmer web server only. Users do not interact directly with this URL.
> * **SharePoint Server URL**: The actual URL users will use to access SharePoint resources.
>
> Warnings:
>
> 1. Please try to ensure that the SharePoint Server URL is valid for all users in all scenarios. A URL of http://sharepoint will not be accessible to users that access from outside the network. Direct links and links to SharePoint documents will use this URL. You may need to use a fully qualified URL in order for this to work in all scenarios for users \(e.g. http://sharepoint.domain.com\).
> 2. The URL that you choose must be configured under "Alternate Access Mappings" in SharePoint Central Administration.
> 3. Do NOT configure more than one URL for the same SharePoint server. This may appear to be successful on the administration screen, but it will lead to erratic behaviour in the SharePoint connector features.

#### **3.** Verify configuration

Once the SharePoint Servers have been added you can the click the Verify button in the Verify configuration section of the screen. This will test the connections to each of the configured Integration Service URLs. If there are any problems an error message will be displayed to you along side the server that failed. Successful connections will show with a green checkmark.

![](../../../.gitbook/assets/4%20%2852%29.jpg)

#### **4.** Available sites

Once the SharePoint Connector has been verified you will see a list of sites available to be integrated into ThoughtFarmer. This list of sites is the root site, plus all the subsites under the configured SharePoint access URL. You can enable or disable specific sites for integration. If a site is not marked as enabled, then no SharePoint integration features will be available for that site.

![](../../../.gitbook/assets/5%20%2819%29.jpg)

### Remove the ScrubHtml filter

In order for users to successfully insert document libraries on intranet pages, the Rich Text Editor filter ScrubHtml must be disabled. Follow the steps below to do this:

1. Go to the **Administration panel**: **Advanced options** section &gt; **Configuration settings** page.
2. Type **rich** in the **Search config settings** field to narrow the config settings results.
3. Find the config setting richTextEditor.customContentFilters.
4. Click in the **Value** column beside the config setting. It will say **DefaultFilters,ScrubHtml**.
5. Delete the **ScrubHtml** filter.
6. Click **Save**.
7. Recycle the application pool on the web server.

