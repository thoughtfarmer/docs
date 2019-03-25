# Active Directory security permissions

### Active Directory security permissions

You can configure the Active Directory security permissions either by using the simple configuration or the advanced configuration.

#### Simple configuration \(Recommended\)

The simple configuration is for the AD Synchronization account to have general read-write access to your Active Directory. 

#### Advanced configuration

Some organizations prefer to restrict this account to have the absolute minimum permissions needed. 

1. The account should be a member of "Domain Users" \(this gives read access to entire AD\).
2. Go to the **Group Policy Management Console** in Windows.
   1. Locate the **Active Directory Container** for your distribution groups. \(There may be many depending on your AD structure.\)
   2. Choose the **Delegation** tab.
   3. Click **Advanced**.
   4. Click **Advanced** again on the dialog that comes up.
   5. Click **Add**, and select the user **Sync Account**.
   6. Assign the following right for "This object and all child objects":
      1. Write All Properties
3. If you wish to also write to users' AD profile fields then "write all properties" is also required on any container that stores user accounts.

\* Group Policy Management Console is an installable feature on Server 2008 & 2012

