# Install the Employee Directory Connector



### Before you begin

To have the information necessary for the setup of the Employee Directory Connector \(EDC\), you need to have already done the following:

* [set up login providers](https://community.thoughtfarmer.com/content/106021)
* [set up the login hostname](https://community.thoughtfarmer.com/content/106021)
* [set up the Active Directory page](https://community.thoughtfarmer.com/content/106020)

Once you've completed the above, follow these steps to install the Employee Directory Connector:

1. Run the latest EDC Manager. The **ThoughtFarmer configuration wizard** window will appear.
2. Select the checkbox\(es\) for the component\(s\) you want to install.

![](../../.gitbook/assets/1%20%2897%29.png)

3.Enter a site name that will be the visible intranet name on your intranet.

![](../../.gitbook/assets/2%20%28107%29.png)



4.Enter a short name for your intranet to be used at the system level. This permanent name will not be visible to users.

5.Select from the dropdowns or fill in the fields to configure and start the ThoughtFarmer web site in IIS. Click **browse** to select the installation path.

![](../../.gitbook/assets/3%20%2812%29.png)

6.See the steps below for the descriptions of the fields to be filled out.

![](../../.gitbook/assets/4%20%2826%29.png)



1. 1. **Main Site URL**: Enter the URL for your ThoughtFarmer intranet.
   2. **API Token**: Go to the ThoughtFarmer Administration Panel. In the box on the right, beside **API token**, click **View**. If there is a value in the **Current token** field, copy it and paste it into the **API Token** field. If there is no value in the **Current token** field, start typing your name in the **Token user** field, and click on it when it appears in the dropdown menu. Then click the **Generate token** button, and copy and paste the token.
   3. **Active Directory ID** \(for forms login\): To get the value you need here, you must have already [set up a Forms login provider](https://community.thoughtfarmer.com/content/106021). Go to the **Administration panel** &gt; **Authentication** section &gt; **Login provider** page. Click on the Forms login provider. Under **Form configuration**, copy the **SAML Configuration ID**, and paste it into the **Active Directory ID** field.
   4. **SSO ID** \(for SSO login\): To get the value you need here, you must have already [set up a SSO login provider](https://community.thoughtfarmer.com/content/106021). Go to the **Administration panel** &gt; **Authentication** section &gt; **Login provider** page. Click on the SSO login provider. Under **Windows configuration**, copy the **SAML Configuration ID**, and paste it into the **SSO ID** field.
   5. **Service UID**: Go to the **Administration panel** &gt; **Users & security** section: **Employee Directory Connector** page. Click on the Active Directory that you are configuring. Under the **Basic information** tab, copy the **Id** value, and paste it into the **Service UID** field.
2. Follow the prompts for the rest of the installation.

