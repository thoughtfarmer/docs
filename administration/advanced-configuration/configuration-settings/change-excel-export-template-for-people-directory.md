# Change Excel export template for people directory



**How to change the Excel export template for** **People Directory**   
  
When you [export the People Directory to Excel](https://community.thoughtfarmer.com/content/105792), you receive information about your employees such as first name, last name, address, and groups they belong to. The Excel export template can be customized so you only see the information you want to see. To do this:

1.Go to the **Administration panel**: **Advanced options** section &gt; **Configuration settings** page. 

2.Type **employee** in the search box to narrow the configuration settings results. 

3.Find the **employee.directory.export.fields**.

![](../../../.gitbook/assets/3%20%2853%29.png)

4.Click in the **Value** column beside the configuration setting. 

![](../../../.gitbook/assets/4%20%2831%29.png)



1. Type the new template ID value\(s\) or remove any existing ones. 
2. Click **Save**. 

\*Please note: this feature works only in ThoughtFarmer versions 7.0.0.36 and beyond.   
  
**Available fields for the Excel export template**

The excel export configuration setting accepts the following People Directory default fields for user's basic information:

_ContentId, UserName, FirstName, LastName, Email, JobTitle, PhoneTel, PhoneMobile, PhoneFax, UserAddressLine1, UserAddressLine2, UserAddressLine3, UserAddressLine4_

It also accepts 3 advanced fields that will display additional information:

* _**Groups**:_ A list of all groups a user belongs to in a single column.
* _**GroupsByType**:_ A list of groups a user belongs to where each group type is a separate column.
* _**Comments**:_ A single column where the data will represent a list of all comments on a user's profile page. It will note the user who made the comment, timestamp, and the comment itself.

Additionally, it accepts values for the "custom field template id" for any custom field added to a user's profile. To find the template ID for these custom fields:

1.Go to the **Administration panel**: **Content** section &gt; **User Profile Custom Fields** page.

2.Under the Label column, find the field group which your desired field belongs in, click the drop down arrow next to it, and select **Fields**. 

![](../../../.gitbook/assets/5%20%2817%29.png)

3.Look under the Template ID column to find the value you are looking for.

![](../../../.gitbook/assets/6%20%2818%29.png)

Please note that **ALL** fields for this configuration are case-sensitive.

