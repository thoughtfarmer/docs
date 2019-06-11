# Understanding ThoughtFarmer Analytics

ThoughtFarmer Analytics is built on Matomo \(formerly known as Piwik\), a downloadable, free \(GPL licensed\) web analytics software platform. It provides detailed reports on your website and its visitors, including: search engines and keywords used, language used, pages visited, files downloaded and more. Matomo \(Piwik\) aims to be an open source alternative to Google Analytics and operates similarly to Google Analytics.  
  
Matomo was chosen as the intranet statistics package for ThoughtFarmer because it comes with a large number of pre-defined reports, is an open sourced project and offers full-data ownership. This allows ThoughtFarmer to customize Matomo and tailor it to track and collect intranet-specific data. This includes data such as user names and page titles, and custom actions like edits, comments, and content creation.

### ThoughtFarmer Analytics data tracking requirements

When a user accesses your intranet with ThoughtFarmer Analytics enabled, a client-side script in the browser collects information on user activity and sends that information to the stats server. For this mechanism to work properly please ensure the following:

* User browsers are set to allow javascript on the intranet.
* Network users do not have the analytics.thoughtfarmer.com URL blocked.
* Ad-blockers are disabled on your browser, or at least your intranet site url and analytics.thoughfarmer.com are white-listed on your ad-blockers.

If there is an interruption in internet service, or if the above configuration is not set up properly, then the analytics data cannot be sent to the server for tracking.

### Matomo unique user definition

For reports where the user's full name is shown, ThoughtFarmer has customized the report to include this information to help track actual unique users. This is not possible in all reports, so those reports that state "unique visitor" use the Matomo definition. These reports are using the default anonymous user configuration that most analytics packages use, including Google analytics.  
  
Matomo reports that include "unique visitors" require that first party cookies are enabled and accepted by your users' browsers. Keep in mind that because of the reliance on cookies, a unique visitor will be defined by some basic assumptions about user behaviour:

* **Every person only uses a single web browser**. Since cookie storage is browser dependent, if someone on the same computer accesses the site from a different browser, they will be counted as a different person. The same is true if a person switches computers. This type of usage would count someone who logs in from home and then logs in later at the office as two unique visitors. Also when the same user visits the site on two different types of devices \(laptop, mobile, tablet\), Matomo detects two unique visitors as well.
* **Cookies are enabled**. If cookies are disabled altogether, there is no way to track that individual and potentially every separate action would trigger a unique visit. Matomo has a fallback mechanism under this scenario that involves IP, computer/OS specifications, and browser type. However, this is less reliable and will still trigger false unique visitors.
* **Users never clear their browser cache**. Clearing the browser cache typically also clears cookies and resets this mechanism as well.

