# Sharepoint Connector setup

### SharePoint Connector setup

The ThoughtFarmer SharePoint Connector is an additional service application that runs on the SharePoint server\(s\) you wish to connect to your ThoughtFarmer Intranet. This page goes through the steps necessary to prepare and install the SharePoint Connector. When you're done with this page, see [Configure the SharePoint Connector](configure-sharepoint-connector.md).

### Add a valid SharePoint Connector license <a id="section1"></a>

In order to enable the SharePoint Connector section of the Administration Panel a valid SharePoint Connector license will need to be added to ThoughtFarmer. Please contact [sales@thoughtfarmer.com](mailto:sales@thoughtfarmer.com) to inquire about pricing. Once you have received a new license you need to apply this to your ThoughtFarmer Intranet:

1. Go to the **Administration Panel**.
2. Select **Edit** in the portlet on the right side, beside your intranet name.
3. Copy and Paste the new license key in the provided area.
4. Click **Save**.

The Administration Panel page will refresh and you should now see the new SharePoint Connector section.

![](../../../.gitbook/assets/1%20%2870%29.png)

### Install SharePoint Connector on SharePoint server\(s\) <a id="section2"></a>

To make a SharePoint site available to ThoughtFarmer you first need to install the SharePoint Connector on the site root. Installing on the SharePoint site root makes all subsites available for connecting to ThoughtFarmer. Once installed, individual subsites can be enabled or disabled for connection as desired from within the ThoughtFarmer Administration Panel.  
  
ThoughtFarmer Support is able to install the SharePoint Connector for you. This requires that Administrator access be granted to the required SharePoint server\(s\). This can be accomplished remotely, or over screenshare. Please contact [support@thoughtfarmer.com](mailto:support@thoughtfarmer.com) to schedule this.  
  
The SharePoint Connector Service will run in the same application pool as the SharePoint site root. It will be configured to run on a designated port during the installation process. By default ThoughtFarmer will use port 8088 for this. Firewall configuration between the web server and SharePoint server may need to be adjusted to allow for this.  
  
When you are finished installing the SharePoint Connector, see the page [Configure the SharePoint Connector](configure-sharepoint-connector.md).  


