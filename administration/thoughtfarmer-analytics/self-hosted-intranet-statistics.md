# Self Hosted intranet statistics

### Self-Hosted Intranet Statistics

The ThoughtFarmer intranet statistics package is based on the Piwik opensource product. It has been customized in order to capture ThoughtFarmer specific data not included in the default Piwik installation.   
  
In order to host your own version of ThoughtFarmer intranet statistics you must use our customized package attached at the end of this page, along with the following instructions. We do not roll out new versions of ThoughtFarmer intranet statistics at the same time as Piwik makes new versions. So **do not** update Piwik unless you get the application folders here.  
  
**On this page:**

* [Installation instructions](self-hosted-intranet-statistics.md)
* [Upgrade instructions](self-hosted-intranet-statistics.md)

### Installation instructions <a id="section1"></a>

**1.\) Install Piwik prerequistes:**

* PHP version 5.1.3 - 5.4 \(versions greater than 5.4 are NOT supported\). You can use 5.4.45 found at [https://secure.php.net/releases/](https://secure.php.net/releases/). 
* MySQL version 4.1 - 5.6 \(versions greater than 5.6 are NOT supported\). You cn use 5.6.29 found at [https://downloads.mysql.com/archives/community/](https://downloads.mysql.com/archives/community/)
* \(enabled by default\) PHP extension [pdo](http://php.net/pdo) and [pdo\_mysql](http://php.net/pdo_mysql), or the mysqli extension

For full prerequisite details along with performance optimization recommendations please see the [Piwik Requirements](http://piwik.org/docs/requirements/) page.   
  
  
**2.\) Install and configure ThoughtFarmer intranet statistics:**

1. Unzip the [intranetstatistics-1.6.zip](https://community.thoughtfarmer.com/content/105870) into a new folder that can run under IIS or Apache.
2. Change the permissions on the folder so that it can run. For IIS the IUSR account should have full control.
3. Create a new site and point it to the unzipped folder.
4. Navigate to the new site in your browser.
5. Follow the 5 minute setup instructions at [http://piwik.org/docs/installation/\#toc-the-5-minute-piwik-installation](http://piwik.org/docs/installation/#toc-the-5-minute-piwik-installation) with 2 exceptions:
   1. Ignore the warning about "File integrity"
   2. Ignore the tracking code that Piwik tells you to install on your website.  A custom version of the tracking code is already built into ThoughtFarmer.

  
**3.\) Configure ThoughtFarmer to connect to your Intranet Statistics installation:**

1. Find "Intranet Statistics" on your ThoughtFarmer Administration Panel
2. Make sure it is enabled
3. Enter your PIWIK SiteID in the "site ID" box. This can be obtained from Settings -&gt; Websites within intranet statistics. 
4. Choose "No" for "Use stats.thoughtfarmer.com"
5. Enter the url of your self hosted Intranet Statistics installation.

* _don't include a trailing /_
* _if Intranet Statistics/Piwik is on a port **other than 80**, include the port number e.g. **our.intranet.local:8088**_
* _if you use SSL \(port 443\) to connect to your intranet, then you must also use SSL to connect to statistics.  Use IIS Manager to configure your SSL certificate.​_

  
**IMPORTANT: If you are logged into Piwik as an administrator, and you see a notification that a new version is available, DO NOT upgrade the new version. It will install a plain copy of Piwik without the ThoughtFarmer modifications.**  
 

### Upgrade instructions <a id="section2"></a>

1. Backup your statistics database in MySQL.
2. Unzip latest intranet statistics package from ThoughtFarmer \(attached below\) into a new directory alongside the current installation.
3. Copy the file config/config.ini.php from the old installation directory to the new one.
4. Change the web site root directory to the new location.
5. Go to the Intranet Statistics site in your browser.
6. Check that the message stated is to _UPGRADE_ the current installation. If it states a new install and you proceed you will delete all existing data.
7. Confirm the upgrade wizard and you will be directed to the new statistics site admin page.

