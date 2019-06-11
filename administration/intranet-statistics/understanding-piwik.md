# Understanding Piwik



Piwik is a client side scripting web analytics package. It operates similarly to Google Analytics. Piwik was chosen as the Intranet Statistics package for ThoughtFarmer because it comes with a large number of pre-defined reports as well as being an open sourced project. This allowed us to customize Piwik in order to tailor it to track and collect intranet specific data. This includes things such as user names, page titles, and also custom actions such as edits, comments, and creations of content, etc…  
  
Piwik also has a self-hosted option available. If you are interested in hosting the ThoughtFarmer customized Piwik package internally on your own network please see the [Self-hosted Statistics](../thoughtfarmer-analytics/self-hosted-intranet-statistics.md) page for details.  
 

#### Piwik data tracking requirements

When a user accesses your intranet with Intranet Statistics enabled, a client side script in the browser will collect information on user activity and send that information to the stats server. For this mechanism to work properly please ensure the following:

* User browsers are set to allow javascript on the intranet.
* Network users do not have the stats.thoughtfarmer.com URL blocked.

  
If there is an interruption in the internet, or the above configurations are not properly set up then the analytics data cannot be sent to the server for tracking.  
 

#### Piwik unique user definition

For reports where username is shown, ThoughtFarmer has customized the report to include this information in order to track actual unique users. This was not possible in all reports and so those reports that state "unique visitor" use the Piwik definition. These reports are using the default anonymous user configuration that most analytics packages use, including Google analytics.  
  
Those Piwik reports that use "unique visitor" require that first party cookies be enabled and accepted by your users browsers. Keep in mind, that because of the reliance on cookies a unique visitor will be defined by some basic assumptions about user behaviour:

* That every person only uses a single web browser. Since cookie storage is browser independent. If someone on the same computer accesses the site from a different browser, they will be counted as a different person. The same is true if a person switches computers. So this type of usage would count someone logging in from home, then later at the office as two unique visitors.
* If cookies are disabled altogether then there is no way to track that individual and potentially every separate action would trigger a unique visit. Piwik has a fallback mechanism under this scenario that involves IP, computer specifications, and browser type. However, this is less reliable and will still trigger false unique visitors.
* Users never clear their browser cache. Clearing the browsers cache typically also clears cookies and resets this mechanism as well.

