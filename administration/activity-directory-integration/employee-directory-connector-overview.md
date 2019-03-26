# Employee Directory Connector Overview

The ThoughtFarmer Employee Directory Connector \(EDC\) allows for connecting your instance of ThoughtFarmer to an external identity provider. This provides the following possibilities:  
 

1. For clients with a cloud instance of ThoughtFarmer, this lets you integrate with your local Active Directory for authentication and user management. 
2. You can use a 3rd party identity provider like OKTA, Azure AD, Google Suite \(TF version 9.1 and higher\) or any other SAML 2.0 identity provider to authenticate to your ThoughtFarmer intranet.
3. You can link multiple combinations of identity providers for your users. This includes multiple Active Directories \(where a trust is not possible\) and hybrid user type scenarios.

  
Here is a simple high-level view of the architecture of a ThoughtFarmer cloud-to-internal AD EDC integration.

![](../../.gitbook/assets/1%20%2875%29.png)

### Authentication

The first component of the EDC is a login site that allows users to use their AD credentials. Once validated, a secure token is passed back to ThoughtFarmer to confirm the identity of the authenticated user. 

![](../../.gitbook/assets/2%20%2822%29.png)

### User management

The EDC Service allows for automatic user management tasks with Active Directory. It will run on your EDC service on your network and send data via secure HTTPS to your ThoughtFarmer intranet by means of API calls. This means no more holes in your firewall to allow for connections in. All updates are pushed from the service directly to ThoughtFarmer when sync operations occur.  
  
The sync operations the service handles are:

1. Bulk user creation
2. Bulk user update \(updates profile field information\)
3. Bulk user deactivation
4. Update synced group memberships
5. Update synced security group memberships

### Advanced multi AD configuration

With the components of the EDC installed and configured it now becomes possible to integrate multiple Active Directories into a single ThoughtFarmer instance. This integration can bring together ADs that otherwise are not connected.   
  
Using an on-premise installation as an example, the following diagram depicts such a configuration. Here 2 ADs are integrated to a single instance of ThoughtFarmer that is being hosted on the internal network of only one of them. Users will see a selection screen when they first access the intranet. They can then choose which identity provider they belong to. That will redirect them to the appropriate login site and initiate the authentication process. Their choice is remembered for subsequent visits and they will be redirected automatically.  
  
**An in-depth look at an on-premise ThoughtFarmer installation integrated with two Active Directories:**

![](../../.gitbook/assets/3%20%2824%29.png)

