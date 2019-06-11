# RSS generation

### RSS generation

ThoughtFarmer has the ability to publish content via RSS feed. If a ThoughtFarmer user has a client that can consume an RSS feed, they can use that to keep up-to-date with their intranet activity.

### Feed content

You can choose how the content of your intranet is published in two ways:

* Titles only, which publishes only the title of the content to the RSS feed
* Titles and body content, both the title and body of the content will be published in the RSS feed

### Custom host URL

This is the URL from which the RSS feed is accessible. Set this value if you want to have the URL accessible from a different URL than your intranet.  
 The URL in the Custom host URL field must resolve to your intranet server.

### Security mode

There are two ways to publish content via RSS: secure and anonymous.

#### Secure

In secure mode, only authenticated users can access the published RSS feeds, and you must use a security-aware RSS client to access secure RSS feeds \(like Outlook 2007\).

#### Anonymous

In anonymous mode, any RSS reader can access the feed. If your ThoughtFarmer installation is accessible from the internet \(outside your firewall\), anonymous mode will expose your feed to the outside world.   
  
You can control what content is published by the RSS feed by changing the security profile associated with the RSS feed. With a security profile set, the RSS feed only publishes content that the profile can access. This allows you to control what content you are feeding out anonymously.

#### Configuring anonymous access

The following steps allow you to configure anonymous access for RSS feeds. If you do set this up, please contact ThoughtFarmer and let us know so we can be careful to preserve this change during upgrades.

1. On the server that ThoughtFarmer is installed on, open up the IIS Manager.
2. In the IIS Manager select the properties of the /Content/RSS folder in the ThoughtFarmer website, then right-click on the folder and choose **Properties.**
3. Select the **Directory Security** tab, then select the button **Edit** under the **Anonymous access and authentication control** section.
4. Make sure that only the **Anonymous access** checkbox is selected and press the **Ok** button, then the **Ok**button on the properties window.
5. Using Windows explorer, navigate to the folder that contains the RSS handler files. In this folder create a web.config file if it does not already exist.
6. Using a text editor set the contents of the web.config file to be:

&lt;?xml version="1.0"&gt;&lt;configuration&gt;    &lt;location path="Notifications.ashx"&gt;        &lt;system.web&gt;            &lt;authorization&gt;                &lt;allow users="\*"/&gt;            &lt;/authorization&gt;        &lt;/system.web&gt;    &lt;/location&gt;    &lt;location path="RecentChanges.ashx"&gt;        &lt;system.web&gt;            &lt;authorization&gt;                &lt;allow users="\*"/&gt;            &lt;/authorization&gt;        &lt;/system.web&gt;    &lt;/location&gt;&lt;/configuration&gt; To re-enable secure RSS follow the above steps in reverse.

