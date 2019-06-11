# Exporting data

In order to analyze or track your data further you can export it in various formats to suit your needs. Each widget and each individual report has a disk icon below it that allows you to choose a method for on-demand export. You can also configure email reports to export data automatically based on a configurable schedule and collection of reports.

### Exporting reports

To export a report simply go through the following steps:

1. Select the **date range** desired for the report \(using the Date range picker\).
2. Go to the widget for the desired report either on the homepage \(if added\) or on the dedicated page for that report.
3. Click on the **Export this dataset in other formats** icon in the footer of the widget.
4. Select the **desired output format** \(detailed below screenshot\).

![](../../.gitbook/assets/1%20%2816%29.png)

**CSV:** This will export the data in comma separated value format. This method will open in Excel and most other spreadsheet applications. It is not recommended for page title reports as there may be commas in the titles themselves that would mangle the format.  
  
**TSV \(Excel\):** This will export the value as tab separated and is the recommended export for Excel.   
  
**XML, HTML, JSON and PHP:** If you would like to export the data to another application or make use of it as a developer, then one of these formats may suit your needs.  
  
**RSS:** To get a feed of the desired report use this option. You can subscribe to this link from a feed reader if you want to get regular updates. This will give you a history of reports based on the time frame selected. For example, if you have a week-long period selected the RSS feed will contain the weekly reports for the last 10 weeks \(configurable\). Also, the feed URL generated here is pre-authenticated, which means you may give the feed URL to someone who does not have a Matomo account and they will be able to receive these reports via RSS as well.

### Filtering your export data

**Report type**

**Standard report**: Your report would not contain any metadata. This is the default export option.   
**Report with metadata**: Your exported report would contain the metadata for each row, for example: logo URLs, country codes, search engine URLs, etc.

**Row limit**

**All**: Your report would includes all records.  
**Custom**: Your report would include only the number of records you select.

**Other options**

**Flatten report**: It is sometimes useful to “flatten” the table so as to compare all elements together.  
**Expand subtables**: It is sometimes useful to display the entire report with all subtables expanded so all elements can be viewed.  
**Format metrics**: Used for adding formatting to your metrics.  
**Show/Hide Export Url**: Clicking this would show/hide the url where of the report you are about to export.

### Email reports

You can also create a digest of reports that can be mailed to you at configurable intervals. Additionally, you can configure this to email reports to anyone. This is ideal if you need to update people who do not have a Matomo account.

**To set up an email schedule:**

1. In the top bar, click **Administration**.
2. Click **Personal** on the left hand side menu and then click **Email reports** to view the list of scheduled reports.
3. Click **Create and schedule a report**.
4. Fill in the **Description** of the report.
5. Select the **Segment** if you would like to send a segmented report \(you need to have segments created for this\).
6. Select the **Email schedule, Report time, Report Via, Report Format**.
7. Fill in the **Send report to** with the email addresses of all intended recipients \(one per line\).
8. Select the report\(s\) that you wish to be included in the mail out.
9. Select **Statistics** to be included in your report.
10. Select **Actions** to be included in your report.
11. Click **Create Report** \(or **Update Report** if you are updating an existing one\).

If your recipients report that they are not receiving the reports from Matomo, ask them to check whether the reports are going to their junk/spam folder. The email [noreply@stats.thoughtfarmer.com](mailto:noreply@stats.thoughtfarmer.com) should be set up as an exclusion.  


