# Customize the login screen

### Customize your intranet's login screen

The login screen is customizable to suit your style and can be localized as well. The main login page will be English but each configured language will also display a link to the localized login page \(if added to the template\). The Forms login page appears similar to the following:

![](../../../.gitbook/assets/1%20%2829%29.png)



The login screen template can be modified on the **Login Templates** page in the **Authentication** section of the **Administration panel**. There are two main areas. The top one contains any **Custom CSS** you wish to define for the templates. The main **Templates** section holds the actual template with a tab for each available language. Display of the templates uses the [Razor View Engine](http://www.asp.net/webmatrix/tutorials/2-introduction-to-asp-net-web-programming-using-the-razor-syntax), as such all templates use HTML mixed with Razor syntax.  
 

### Modifying the Template

There are a few components in the template that need to remain in order for the customization to work properly. At a minimum the login template needs the following:

```text
<validation /> 
<login />
<localizedLinks />
```

Beyond that you can add any messages, styles, or layout to suit your desired look and feel. All custom code should be inside the @section declaration.

### Variables in Razor

There are a few variables that can be accessed from the Login template. Each of them can be accessed through the Model class. To output the variable as a string in the page use the format _@Model.Variable_. To use it as a programmatic variable or argument in the template use _Model.Variable_. The available variables are:

* **Model.LoginLogoUrl**: This is the URL for the logo displayed on the login page. This logo is stored on the Admin Theme page on the Site settings tab.
* **Model.WelcomeMessage**: This is the default welcome message for the page. This corresponds to the Language Label SignIn_WelcomeMessage_. You can choose to put this on each page to use ThoughtFarmer's localization. Alternatively, you can choose not to include it and manually create your own message for each language.
* **UnableToSignInMessage**: This is a message to prompt the user to contact the system administrator if they are having problems. This corresponds to the Language Label _LoginUnableToLoginMessage_.
* **Model.ApplicationName**: This is the application name that is set up in the Config setting _name_.
* **Model.Culture**: This is the language of the current login page.

