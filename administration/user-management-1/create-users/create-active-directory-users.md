# Create Active Directory users



### How to create Active Directory users

Creating Active Directory users can be done manually, or, if Active Directory integration is configured, using one of the automated methods described below.

**Go to**:

* [Create users without Active Directory integration](create-active-directory-users.md)
* [Create users with Active Directory integration](create-active-directory-users.md)
  * [Manual user creation](create-active-directory-users.md)
  * [On-demand user creation on first login](create-active-directory-users.md)
  * [Bulk user creation using daily scheduled tasks](create-active-directory-users.md)
  * [On-Demand bulk user creation](create-active-directory-users.md)

###  Create users without Active Directory integration <a id="section1"></a>

1. Go to the ThoughtFarmer **Administration Panel**: **Users & Security** section &gt; **Create user** page.
2. In the **Account Type** section ensure that "Active Directory user" is selected.
3. Select the appropriate Active Directory from the **Active Directory configuration** dropdown menu.
4. Enter the **username** in the provided text field. This must be pre-fixed with the Domain for the user account \(e.g. DOMAIN\username\).
5. Enter the user's account information in the provided text fields \(First and last name are required at a minimum\).  

![](../../../.gitbook/assets/1%20%28100%29.png)



6.Click **Create user**.

### Create users with Active Directory integration <a id="section2"></a>

With Active Directory Integration configured and automatic user creation enabled there are 4 ways to create users:

* [Manual user creation](create-active-directory-users.md)
* [On-demand user creation on first login](create-active-directory-users.md)
* [Bulk user creation using daily scheduled tasks](create-active-directory-users.md)
* [On-demand bulk user creation](create-active-directory-users.md)

#### Before you begin check to ensure that:

1. The user has an active Domain account.
2. The user account is part of the AD Group that ThoughtFarmer is configured to sync with on the Employee Directory Connector page \(if using automatic user creation\).
3. The user account has the first and last name attributes in AD populated \(givenName, and sn respectively\).
4. Any other AD user account attributes you wish to be auto-populated to a user's ThoughtFarmer profile are configured in the [AD Field Mappings](../../activity-directory-integration/active-directory-field-mappings/) portion of the Administration Panel.

### Manual user creation <a id="section2a"></a>

1.Go to the ThoughtFarmer **Administration Panel**: **Users & Security** section &gt; **Create user** page.

2.In the **Account Type** section ensure that "Active Directory user" is selected.

3.Select the appropriate AD configuration from the **Active Directory configuration** dropdown menu.

4.Enter the user's Domain username in the format Domain\username. \(for cloud or DMZ installations use the format DomainController.domain.com\username\)

5.Click **Load account information**.

6.Verify that the correct user information was pulled in. The Account information fields will fill in automatically. Rectify any errors if they are shown.

![](../../../.gitbook/assets/1%20%2891%29.png)



7.Click **Create user** at the bottom.

### On-Demand user creation on first login <a id="section2b"></a>

This is the first of the automated user creation options. This requires that the user's AD account is active and a part of the synced with group. When the user first logs in to the system ThoughtFarmer will automatically pull all AD field mappings and create a profile page for that user.

Note: If you are relying on this method to populate ThoughtFarmer, users will not show up in the Employee Directory until they have logged in for the first time.

### Bulk user creation daily scheduled tasks <a id="section2c"></a>

A daily scheduled task can be created for a number of Active Directory features. When the Bulk Create option is configured the [ThoughtFarmer Service](../../behind-the-scenes/thoughtfarmer-service.md) will create a user's profile page in ThoughtFarmer for every user in the synced with AD group that doesn't already have one. Please see [AD synchronization tasks](../../activity-directory-integration/active-directory-synchronization-tasks.md) for more info.

### On-Demand bulk user creation <a id="section2d"></a>

The On-Demand bulk user creation works exactly like daily scheduled tasks except that it is triggered by an administrator.

#### Trigger on-demand bulk user creation

1. Go to the **Administration Panel**: **Users & Security** section &gt; **Employee Directory Connector** page.
2. Click on the Active Directory that you want to trigger bulk user creation for.
3. Scroll down to the On-Demand synchronization section.
4. Check **Bulk create users**.
5. Click **Synchronize now.**

![](../../../.gitbook/assets/2%20%2857%29.jpg)

It may take some time for the [ThoughtFarmer Service](../../behind-the-scenes/thoughtfarmer-service.md) to complete the update. This depends on the number of users in the synced-to AD group and the server resources available. Your total licensed user count will change when the update is complete.

