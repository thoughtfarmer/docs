# Date selection and report generation



All reports and widgets in Matomo will display data for a selectable time range. When you first log in, the date range will default to the current day's set of data. You can adjust this to globally set all the reports to show data for the desired range.

### Date range selection <a id="section1"></a>

The date range selector is easily accessible in the same spot on every page. Whatever range or single date is shown here will affect every report and widget throughout the site. So you only need to select the date once, and you can then browse from tab to tab, report to report, to view and export data for that date range.  
  
  
You can select a pre-determined date range for a day, week, month or year. These reports are pre-compiled for performance and will be delivered the fastest. See **Date selection and report generation** in the next section for details. You can also choose a custom date range.

**To change to a pre-compiled date range:**

1. Click the **date range dropdown**.
2. Select the **desired length** \(day, week, month, year, custom date range\). Switching this length will change the reports to the most recent period for that length \(i.e. this year, this month\).
3. If you want a range in the past then select the desired month and year from the calendar.
4. Click in the month area to choose the desired past range.

**To change to a custom date range:**

1. Click the **date range dropdown**.
2. Select **Date range** under the period column. This will bring up a second calendar for selection.
3. Choose the **start date** from the left calendar, and the **end date** from the right calendar.
4. Select **Apply date range**.
5. For performance reasons we would not suggest selecting long date ranges.

### Date selection and report generation <a id="section2"></a>

All of the daily, weekly, monthly, and yearly reports are pre-compiled to save server performance and delivery speed. So selecting anything in these ranges should bring back the reports quickly. If you require a custom date range, keep in mind that these reports are generated on demand and will take significantly longer to deliver. If your custom date range is too long it may generate an error if it exhausts the memory limits of the server.  
  
The data Matomo collects will only be available in the pre-compiled reports at certain times. If you want the latest data for a pre-compiled report then take into account the following report generation schedule:

* **Daily reports:** Every 15 minutes
* **Weekly stats**: Hourly
* **Monthly and Yearly stats:** Nightly

