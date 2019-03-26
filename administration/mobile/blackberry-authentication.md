# Blackberry Authentication

### How to configure Blackberry authentication for your intranet

If you have Blackberry Enterprise server at your business you can configure the Blackberry MDS Connection service to support Integrated Windows authentication. This will allow users to access resources on your organization's network using Blackberry devices without requiring them to type a username and password each time.  
  
Before you configure the BlackBerry MDS connection service to support Integrated Windows Authentication, you must do the following:

* Create a Microsoft Active Directory account in each Microsoft Active Directory domain that includes resources for which you want to turn on Integrated Windows authentication.
* Configure constrained delegation for the Microsoft Active Directory accounts so that they delegate access to each intranet site or network shared folder in the Microsoft Active Directory domain.
* Configure a two-way trust between the Microsoft Active Directory domain that the BlackBerry MDS Connection Service is running on and other Microsoft Active Directory domains in other forests that the BlackBerry MDS Connection Service must connect to.
  * The S4U2proxy extension that the BlackBerry MDS Connection Service uses to retrieve the Kerberos service tickets for users requires a two-way trust between Microsoft Active Directory domains.
* After you turn on Integrated Windows authentication and specify a Microsoft Active Directory account in the BlackBerry Administration Service, you must:

1. specify web address patterns for the network resources that you want to permit users to access,
2. create a pull rule for web address patterns,
3. permit access to the web address patterns using the pull rule,
4. assign the pull rule to users or a group.

### Prerequisites to configuring the Microsoft Active Directory account to delegate access

* Verify that you configured Integrated Windows authentication for the application server that hosts the intranet site.
* Verify that the application server that hosts the intranet site and the web application that runs on the application server support Kerberos authentication.
* Verify that you have permission to update the Microsoft Active Directory account in Microsoft Active Directory.
* Verify that you have access to the Windows Server setspn tool that is included with the Windows Server Support Tools. For more information about the setspn tool, visit [Setspn Overview](http://technet.microsoft.com/en-us/library/cc731241%28WS.10%29.aspx).
* If you did not configure a Microsoft Active Directory account to delegate access to an intranet site or shared folder, in Microsoft Active Directory, you must create a Microsoft Active Directory account that should have the following conditions:
  * Has a password that meets the security requirements of your organization
  * The user is not required to change their password the next time they log in
  * The user's password never expires.
* If you configured a pool of application servers to host the intranet site, and the pool is running on Microsoft IIS and is located behind a load balancer, specify a user account \(also known as the identity\) for the pool that hosts the intranet site. For more information, see [http://technet.microsoft.com/en-us/library/cc771170\(WS.10\).aspx](http://technet.microsoft.com/en-us/library/cc771170%28WS.10%29.aspx)

### Configure the Microsoft Active Directory account to delegate access to an intranet site

1. If a pool of application servers hosts the intranet site, and the pool is running on Microsoft IIS and is located behind a load-balancer, use setspn or ADSI to add the SPN's of the intranet site to the user account \(also known as the identity\) of the pool. You must also configure the SPN's using the FQDN and the name of the intranet site that users type into their browsers \(for example, if users type http://intranet\_site in their browsers, the name of the intranet site is intranet \_site\).
2. In Microsoft Active Directory, if the Delegation tab does not display in the Microsoft Active Directory account properties, update the default HOST SPN registrations for the Microsoft Active Directory account.
3. In the Microsoft Active Directory account properties, on the Delegation tab, configure the following settings:
   * trust this user for delegation to specified services only
   * use any authentication protocol.
4. Click Add.
5. Perform one of the following tasks:
   * If a pool of application servers hosts the intranet site, and the pool is running on Microsoft IIS and is located behind a load-balancer, select the user account that runs the application pools in the Microsoft IIS servers.
   * If the intranet site is hosted by one application server, select the application server that hosts the intranet site .
6. Select the HTTP service type for the user account or application server that you specified.
7. Repeat steps 1 to 6 for each intranet site for which you want to turn on integrated Windows authentication.

### After you finish

* If required, configure BlackBerry MDS Connection Service to use a Microsoft Active Directory account when the messaging server is in a remote Microsoft Active Directory domain.
* Turn on Integrated Windows authentication when users access resources on your organization's network.

For more detailed instructions please consult the following [BlackBerry documentation.](http://docs.blackberry.com/en/admin/deliverables/25767/Configuring_high_availability_for_BES_components_606291_11.jsp)  


