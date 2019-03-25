# Set up login providers

### Types of login providers

On the **Administration panel**: **Authentication** section &gt; **Login provider** screen, there are three sections for login providers.

* **Internal Providers:** Internal login providers use the same host as your intranet. No EDC site is required for the internal login provider to work.
* **External Providers:** External login providers use a different host location that will redirect users to the intranet after successful authentication. They can be Windows SSO or AD providers that authenticate via the Employee Directory Connector site. They can also be other SAML identity providers, such as Salesforce.
* **Default Provider:** The default provider is an internal identity provider that is pre-configured as a fallback, in case none of the other login providers match the current request host name. The default provider is always set to enabled.

### ​Set up login providers

1. Go to the **Administration panel**: **Authentication** section &gt; **Login provider** page.
2. Click **Add New** beside the heading under which you want to add a login provider.
3. In the dialog box that appears, select the **radio button** for the type of login provider you are adding:**ThoughtFarmer form**, **Windows single sign on**, or **Custom SAML**.
4. Click **Next** in the dialog box. You will be taken to the **Add login provider** screen.
5. In the **Name** field, enter the name of your login provider.
6. In the **Description** field, enter a description that will indicate to your users which login provider they need to choose to be able to login.
7. \(Optional\) Click **Choose File** to choose an image to display for this login provider. Browse for the image file, select it and click **Open**.
8. Under **Settings**, enter your main site URL in the **Hostname** field.
9. \(Windows SSO and Custom SAML only\) In the **Login \(Provider complete\) hostname** field, enter the hostname of your login site as configured on your server. \(You first need to create a DNS entry that points to your login server.\)
10. Under **Form/Windows/Custom SAML Configuration**, select the appropriate Active Directory/External User Store from the **Active Directory/External user store configuration** dropdown.
11. \(Optional\) For Thoughtfarmer Form internal login providers only, select the **Stay signed in** checkbox to allow the intranet to remember a user's computer and keep the user signed in when they return. If applicable, enter the number of days the user can be remembered for, and IP ranges from which users can be remembered. \(See **Stay signed in** heading below for more information.\)
12. \(Optional\) Select the radio button for the desired level of **Guest access** to allow users without an account, who have successfully authenticated, to view the site as a guest. \(For more information, see [Guest users](../user-management-1/guest-users.md).\)
13. \(Optional - External only\) **Advanced SAML Options**: see heading below for more information.
14. Click **Save**.

When you return to the page after clicking **Save**, a SAML configuration ID will have been generated. You will need this ID for setting up the Employee Directory Connector on your server. \(When [setting up the EDC](install-the-employee-directory-connector.md), the SAML configuration ID gets entered in the SSO ID field of the ThoughtFarmer Configuration Wizard.\)

### Advanced SAML Options

In this section you can fine-tune your external Identity Provider configuration. You can adjust every part of SAML protocol, including encryption, signing and Single Sign Out.

### Stay signed in

In **Step 11** above, an administrator can change the value of the **Stay signed in** checkbox \(Allow the intranet to remember a user's computer and keep the user signed in when they return\) on the Login providers admin screen. If an administrator changes this setting for an External site, the administrator must flush the cache of the application pool on the server that has the Employee Directory Connector on it, in order for the change to take effect.  
  
Administrators can add an IP range, so that users can only stay signed in to the intranet when at a certain location, such as the office.

### Automatic Sign Out

On the **Login providers** page, under the **Automatic Sign Out** heading, you can enter the number of minutes of inactivity after which users who have not selected "Stay signed in" will be logged out.

### Default Provider

You can edit the current default provider or replace it with another type. To edit the current default provider, click on the Name of the default provider. You will be taken to the Edit login provider page where you can edit the details and then click Save at the bottom of the page.  
  
To replace the default provider click **Replace** in the Default Provider section and follow the instructions under the **Set up login providers** heading.  


