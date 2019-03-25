# Feature requiring write access to Active Directory

### User profile field mapping where ThoughtFarmer is the data owner 

User profile field mapping where ThoughtFarmer is the data owner requires write access to be enabled for the ThoughtFarmer AD service account. The settings for this account are configured on the individual [Active Directory](./) page.  
  
ThoughtFarmer can perform a two way mapping between AD user attributes and ThoughtFarmer profile fields. If ThoughtFarmer is set as the data owner then user updates to these fields will write back those changes to AD. This requires write access permissions for the AD service account as well as write access enabled in ThoughtFarmer. Please see [Active Directory field mappings](../active-directory-field-mappings/) for more information.  
  
With no write access enabled, all fields that are synced must have AD as the data owner. Any changes made by users will be overwritten when the [Active Directory synchronization tasks](../active-directory-synchronization-tasks.md) "Bulk update users" is run.

