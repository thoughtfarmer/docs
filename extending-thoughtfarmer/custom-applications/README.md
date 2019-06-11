# Custom applications

Before considering a custom application please first consider the Custom Card and Public REST API method. Please see the [Custom cards](../thoughtfarmer-custom-cards/) section for details.  
  
Custom applications are currently only supported for on-premise ThoughtFarmer instances. If you have a cloud instance and would like to create your own custom application, please first submit a request ticket to [helpdesk@thoughtfarmer.com](mailto:helpdesk@thoughtfarmer.com) before you begin development. Professional Services costs will be incurred to audit and deploy custom applications to the cloud.Custom applications in ThoughtFarmer behave exactly like regular cards and global cards. However, their code comes from a completely different source deployed as a sub-application. A custom sub-application can be added via IIS to your ThoughtFarmer instance. This application can be developed using any IIS supported technology; ASP.NET, .Net Core, or even PHP if you have the right plugins installed. 

### Key benefits

A custom application is suitable for a number of scenarios:

* Using the custom card model and the ThoughtFarmer Public REST API is not possible. 
* The complexity of the customization is high. 
* You wish to integrate with a 3rd party database.
* The customization requires server side code.
* You want to include the code into your own version control systems.

ThoughtFarmer user information and card configuration can be passed along to the sub-application. However, this will have to be carefully setup. You can use our [example application](adventureworks-example-application/) as a template.

### **In this section:**

* [Custom application configuration](configure-a-custom-application.md)
* Development tutorial and template [AdventureWorks example application.](adventureworks-example-application/)

