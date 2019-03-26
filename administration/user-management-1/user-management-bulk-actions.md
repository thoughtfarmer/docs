# User management bulk actions



### User management actions overview <a id="section2"></a>

You can apply actions to many users at once, or to a single user. To do this go to the **Administration panel**: **Users & security** section &gt; **User management** page. Available actions are shown in the "Choose an action..." dropdown.

### Apply bulk user management actions

1. Use the filter, sort, and query tools to find the desired user or set of users \(see [Find users](https://community.thoughtfarmer.com/content/105964) for more info\).
2. Select the checkbox beside the users you wish to apply the action to \(the top left checkbox will select all users on the current page\).
3. Select the appropriate user action from the dropdown box "Choose an action..."
4. Click **Go**.

![](../../.gitbook/assets/1%20%2810%29.png)



| Bulk user management action | Applies to user type | Applies to status | Additional notes |
| :--- | :--- | :--- | :--- |
| **Activate user**: Sets the status of the selected users to "Active". Please see [Activate users](activate-users.md) for more info. | All | Inactive | [Profile only users](activate-profile-only-users.md) should be made active by inviting them or setting a password.  Expired users must be sent a new invitation.  Invited users will become active once they access the link in their invitation email and set their own password. |
| **Deactivate user**: Sets the status of the selected users to "Inactive". These users will no longer be able to log in. Please see [Deactivate users](deactivate-users.md) for more info. | All | Active | Profile only, expired and invited users should be [deleted](https://community.thoughtfarmer.com/content/105943) instead, as they are not active. |
| **Delete user**: This deletes the selected user profiles from ThoughtFarmer. Please see[ Delete users](delete-users.md) for more info. | All | All | Users' content must first be deleted, or have been changed to another owner \(either manually or using the Change Owner tool\). |
| **Undelete user**: This undeletes the selected user profiles. Please see [Undelete users](undelete-users.md) for more info. | All | Deleted | When a user is undeleted, their account status is set to inactive. |
| **Invite user to activate account**: This sends out an invitation email to the selected users. Please see [Activate a Profile only user](activate-profile-only-users.md) for more info. | Regular | Profile only Expired | If a user is already invited you must first [cancel the existing invitation](cancel-and-resend-invitations.md). |
| **Cancel user's invitation to activate account**: This cancels existing invitations for the selected users. Please see[ Cancel and resend invitations](cancel-and-resend-invitations.md) for more info. | Regular | Invited Expired | You must cancel a user's existing invitation before you can send a new invitation. |
| **Force password change on next login**: This forces the selected users to change their password the next time they log in. | Regular | Active | Once this action is taken the user will show with a icon beside their name. |
| **Cancel force password change:** This will clear the "Force password change on next login" for the selected user accounts. Please see [Cancel force password change](cancel-force-password-change.md) for more info. | Regular | Active | Only applies to users that have been flagged to change their password. Noted by the icon beside their name. |

