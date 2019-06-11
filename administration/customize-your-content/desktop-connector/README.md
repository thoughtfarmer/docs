# Desktop connector

### Set up and update the Desktop Connector

The Desktop Connector is a software application that runs behind-the-scenes on your computer and allows you to edit documents from your intranet on your desktop. The ThoughtFarmer Desktop Connector is not enabled by default on new installs.

### System Requirements

The Desktop Connector works on all Windows and MacOS browsers that are supported by ThoughtFarmer. The Desktop Connector is not supported on mobile devices.

### Enable the Desktop Connector <a id="enableDesktopConnector"></a>

1. Go to the **Administration panel**: **Advanced options** section &gt; **Desktop Connector** page.
2. Click **enable** to enable the Desktop Connector.  ![6.7Admin8838EnableDC.png](https://community.thoughtfarmer.com/imagethumb/266648770000/16500/481x36/False/6.7Admin8838EnableDC.png)

### Installing the Desktop Connector <a id="installDesktopConnector"></a>

The Desktop Connector will automatically prompt the user to install it when they try to open any document for editing. See [how to open a file for editing](../../../using-thoughtfarmer/add-and-edit-files/open-and-lock-a-file-for-editing.md) for end user Desktop Connector instructions.

### Check for new versions of the Desktop Connector <a id="checkDesktopConnectorVersion"></a>

1. Go to the **Administration panel**: **Advanced options** section &gt; **Desktop connector** page**.**
2. A message specifying your current version of Desktop Connector is displayed. ![8.0Admin15455DCVersion.jpg](https://community.thoughtfarmer.com/imagethumb/284626630000/16501/400x40/False/8.0Admin15455DCVersion.jpg)  
3. If a newer version of the Desktop connector is available a message is displayed. e.g. A newer version of the desktop connector is available \(eg. version 3.0.0.3\)
4. Click the **button** "Configure _ThoughtFarmer_ to use the latest version" where _ThoughtFarmer_ is the name of your intranet.

When you upgrade to a newer version, all users who have the Desktop Connector installed will also be prompted to upgrade the next time they start the Desktop connector application.  
 

### Tip: Unlocking a file for a user

A user may come to you as an intranet administrator complaining that they cannot open a file for editing. If there is a lock icon beside the file name, this means that someone else has the file open for editing. Other users are prevented from opening the file for editing to prevent multiple file versions and duplication of work. Those users will not see the option to Open for editing in the file menu.  
  
On the actual file page, a message will indicate who has the file open for editing.

![](../../../.gitbook/assets/1%20%2896%29.png)

If the person who was editing the file is unable to close the file and click Done editing on the intranet \(perhaps because they have left work for the day\), an administrator can unlock the file. However, if an admin unlocks the file, any changes to the file made by the person who was editing it previously will be lost. To unlock the file, go to the individual file page in Admin mode and click the **Remove lock** button below the file name.

![](../../../.gitbook/assets/2%20%2813%29.png)

