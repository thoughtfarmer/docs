# AdventureWorks example application

This sample provides a template and simple application to get you started on ThoughtFarmer custom application development. 

For details on the code provided please see the [_**Developer notes page**_.](developer-notes.md) **On this page:** 

* [Requirements](./)
* [Database setup](./)
* [Build the application](./)
* [Deploy the application](./)
* [Configure the cards](./)

### Requirements <a id="requirements"></a>

You should have a ThoughtFarmer development instance along with access to the SQL server instance hosting its data. For development you will require the following:

1. [Visual Studio](https://visualstudio.microsoft.com/downloads/)
2. The latest [.Net Core SDK](https://dotnet.microsoft.com/download)
3. [AdventureWorks2017 OLTP test database](https://docs.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-2017#oltp-downloads). The .bak file should be restored on your SQL instance.
4. Download and extract the sample [ORC.TF.Custom.AdventureWorksSample.zip](https://community.thoughtfarmer.com/attachment/199425300000/111855/ORC.TF.Custom.AdventureWorksSample.zip)

### Database setup <a id="database"></a>

Once the _**AdventureWorks2017**_ database is downloaded and restored we can update a record in the \[HumanResources\].\[Employee\] table so that it is linked to a ThoughtFarmer user.  
  
**Single user script:**

```text
update [HumanResources].[Employee]
set LoginID = 'TFUserName',
VacationHours = 110,
SickLeaveHours = 38
where LoginID = 'adventure-works\roberto0'
```

**Multi-user script:**  
This will associate test data for all your users. This is helpful if you would like to test this on multiple accounts, or to extend the custom application in other ways.

```text
update aw
set aw.LoginID = ps.Username from [AdventureWorks2017].[HumanResources].[Employee] aw
inner join [THOUGHTFARMER-DATABASENAME].[dbo].[User] ps on ps.UserID = aw.BusinessEntityID 
```

###  Building the application <a id="build"></a>

The sample application can be built using the tools provided with Visual Studio 2017 and the .Net core SDK.  
  
Because this application is a sub-application of the main ThoughtFarmer site, the publishing process for the code is slightly different. To publish from the command line execute \(from the folder containing the file _**ORC.TF.Custom.AdventureWorksSample.sln**_\)

```text
dotnet publish /p:IsTransformWebConfigDisabled=true
```

![](../../../.gitbook/assets/8%20%288%29.png)

### Deploy the application <a id="deploy"></a>

The publish folder will be found in a subfolder of the application. It is typically found in \bin\Debug\netcoreapp2.1\publish. The exact location may vary depending on your specific settings. You will need to zip this folder and deploy it to your ThoughtFarmer server.  
  
This folder is the one you will use to add a new sub-application in IIS. Please see [Configure a custom application](../configure-a-custom-application.md) for more details.

### Configure the cards <a id="coinfigure"></a>

This example comes with 2 available custom cards. One is a **Global application** meaning that it always runs on all pages. The other is a **Page template application.** These will behave like other custom cards and can be added to any page template anywhere on the site.  
  
Please see [Configure an application](../configure-a-custom-application.md) for details on setting this up.

#### AdventureWorks Employee

If the currently logged in user accesses their own profile page, and their username matches data found in the \[AdventureWorks2017\].\[HumanResources\].\[Employee\] table, then a custom tab will be added to display data and emulate a basic sick\vacation day request feature.  
  
**Configuration:**

1. Add a new Global application
2. **Server url:**
   * /ccadventureworks/api/employee
3. **Javascript url:**
   * /ccadventureworks/js/employee.jsx
4. Save the card.
5. Activate the card.

Now if you go to your profile page, and you have set up the data properly you should see the added tab on your profile.

![](../../../.gitbook/assets/9%20%2814%29.png)

#### AdventureWorks Category

This customization will pull in data from the AdventureWorks2017 database. It also demonstrates how to pass along configuration from an instance of a card to the custom application code. 

**Configuration:**

1. Add a new Page template application.
2. **Server url:**
   * /ccadventureworks/api/products
3. **Javascript url:**
   * **​​​​​​​​​​​​​​**/ccadventureworks/js/products.jsx
4. **CSS url**:
   * **​​​​​​​​​​​​​​​​​​​​​**/ccadventureworks/css/products.css
5. Go to **Details** &gt; **Default configuration** and add:
   * { "configuration": "" }
   * Check the option "_**Allow card configuration on edit page**_".
6. Save the card.
7. Activate the card.
8. Go to any page and add the Custom card to the page. 
9. Click the gear icon to modify the configuration.
10. Update the configuration:
    * { "configuration": "Clothing" }
    * Supported values are Bikes, Clothing, Components, Accessories as taken from the \[Production\].\[ProductCategory\] table from the AdventureWorks2017 database.
11. Save the changes.

Now the page should show the values wherever you placed the card on the template.

![](../../../.gitbook/assets/10.png)



