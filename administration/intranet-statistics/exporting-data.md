# Exporting data

In order to analyze or track your data further you can export it in various formats to suit your needs. Each widget, and each individual report has a disk icon below it that will allow you to choose a method for on demand export. As well, you can configure email reports to export data automatically based on a configurable schedule and collection of reports.  
  


#### Exporting reports

To export a report simply go through the following steps:

1. Select the date range desired for the report \(using the Date range picker\)
2. Go to the widget for the desired report either on the homepage \(if added\) or on the dedicated page for that report.
3. Click the disk icon at the bottom of the widget.
4. Select the desired output format \(detailed below\).

  
**CSV:** This will export the data in comma separated value format. This method will open in excel and most other spreadsheet applications. However, it is not recommended for page title reports as there may be commas in the titles themselves that would mangle the format.  
  
**TSV \(Excel\):** This will export the value as tab separated and is the recommended export for Excel.   
  
**XML, Json and Php:** If you would like to export the data to another application or make use of them as a developer, then one of these formats may suit your needs.  
  
**RSS:** To get a feed of the desired report use this option. You can subscribe to this link from a feed reader if you want to get regular updates. This will give you a history of reports based on the time frame selected. For example, if you have a week period selected the RSS feed will contain the weekly reports for the last 10 weeks \(configurable\). Also, the feed URL generated here is pre-authenticated, which means you may give the feed URL to someone who does not have a Piwik account and they will be able to receive these reports via RSS as well.  
  
  


#### Email reports

You are also able to create a digest of reports that can be mailed to you at configurable intervals. Additionally, you can configure this to email reports to anyone. So this is ideal if you need to update people who may not necessarily have a Piwik account.  
  
**To set up an email schedule:**

1. Click **Email reports** in the very top of the Piwik site.
2. Click **Create and schedule a report**.
3. Fill in the **Description** of the report.
4. Select the **Email schedule** \(see details below\).
5. Fill in the **Send report to** with all email addresses of intended recipients \(one per line\).
6. Choose the **Report Format** \(PDF will send as an attachment, HTML will send directly in the email\).
7. Select the report\(s\) that you wish to be included in the mail out.
8. Click **Update Report**.

  
If your recipients complain that they are not receiving the reports from Piwik then be sure it is not ending up in their spam folder. The email [noreply@stats.thoughtfarmer.com](mailto:noreply@stats.thoughtfarmer.com) should be set up as an exclusion.

