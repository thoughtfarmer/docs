# Permission rules

### Permissions rules

Each of the following security roles has progressively more permissions:

* Guest
* View-only
* Editor
* Owner
* Admin

Guest is a security profile that can only have view only permissions granted, but may have no permissions. A user who is an Administrator can view and edit everything on the intranet when they are in Admin mode, but when they are not in Admin mode, they access the intranet with whatever permissions have been granted to them.  
  
The security roles are **context sensitive** -- you can have no permissions on one page \(you won't see it or even know it exists\), the view-only role on another page, the editor role on another, and the owner role on another.

### Security matrix

|  | Guest | Viewer | Editor | Owner | Admin |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **View page** | Yes | Yes | Yes | Yes | Yes |
| **View comments** | Yes | Yes | Yes | Yes | Yes |
| **View attachments** | Yes | Yes | Yes | Yes | Yes |
| **View draft/private page** | No | No | No | Yes | Yes |
| **View future-published page** | No | No | No | Yes | Yes |
| **Create subpage** | No | No | Yes | Yes | Yes |
| **Edit page** | No | No | Yes | Yes | Yes |
| **Delete page** | No | No | Yes | Yes | Yes |
| **Comment** | No | Yes | Yes | Yes | Yes |
| **Delete own comment** | No | Yes | Yes | Yes | Yes |
| **Delete any comment** | No | No | No | Yes | Yes |
| **Attach** | No | No | Yes | Yes | Yes |
| **Edit any attachment** | No | No | Yes | Yes | Yes |
| **Delete own attachment** | No | No | Yes | Yes | Yes |
| **Delete any attachment** | No | No | Yes | Yes | Yes |
| **View unshared Bookmarks** | No | No | No | Yes | Yes |
| **View page Security Settings** | No | No | Yes | Yes | Yes |

**Note:** Owner privileges apply to all content explicitly marked as owned by a user, as well as all content in a user's profile page. A user can delete and edit all content under their profile page, even if another user created it.

###  Inactive or deleted users matrix

|  | Guest | Viewer | Editor | Owner | Admin |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **View inactive's Profile** | No | No | No | No | Yes |
| **View inactive's page** | Yes | Yes | Yes | Yes | Yes |
| **View inactive's comments** | Yes | Yes | Yes | Yes | Yes |
| **View inactive's name** | Yes | Yes | Yes | Yes | Yes |
| **View inactive's photo** | Yes | Yes | Yes | Yes | Yes |
| **View deleted's Profile** | No | No | No | No | No |
| **View deleted's page** | N/A | N/A | N/A | N/A | N/A |
| **View deleted's comments** | Yes | Yes | Yes | Yes | Yes |
| **View deleted's name** | No | No | No | No | No |
| **View deleted's photo** | No | No | No | No | No |

  
**Note on names and photos:** The names and photos of inactive users are not linked to their profile page - they are linked to the list of all people \(/people/\). For deleted users, their name is replaced with \(user deleted\) and their photo with the default photo.

**Note on inactive user's pages:** The content created by inactive people - pages, comments, attachments - always remains available until it is specifically deleted. In the case of child pages of an inactive person's profile page, non-admins can only reach it via search or if they know the URL.

You can't delete a user who still owns pages.

Also see [Search and navigation](search-and-navigation.md).  


