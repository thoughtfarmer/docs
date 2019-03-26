# Purge deleted information

### Purge deleted users and pages from your intranet

When pages or users are deleted from ThoughtFarmer, they are still recoverable by intranet administrators using the Restore content or User management pages of the administration panel.  
  
However it is possible to permanently delete pages and users from the database, using the **Purge deleted information** page. You may want to purge deleted information if limited disk space is a concern. It is strongly recommended that you have an up-to-date backup prior to purging the database.

### Purge deleted users

**Caution!** Performing this action will permanently delete information from the database and render that information unrecoverable.

1. Go to the **Administration panel**: **Content** section &gt; **Purge deleted information** page.
2. The number of users to be purged is indicated above the **Purge deleted users** button.
3. Click on the **Purge deleted users** button to permanently delete deleted users.
4. Click **OK** to confirm the purge.

### Purge deleted pages

**Caution!** Performing this action will permanently delete information from the database and render that information unrecoverable.

1. Go to the **Administration panel**: **Content** section &gt; **Purge deleted information** page.
2. Move the sliders back and forth on the bar to select which pages to purge based on the date when they were deleted. 
3. Click on the **Purge deleted pages** button to permanently delete deleted pages.
4. Click **OK** to confirm the purge.

### Status indicator

The Status will say different things depending on the state of the purge.

* **Idle:** No purge is currently running.
* **Processing \# out of \#:** Indicates how far along the purge is in the total number of items to be purged.
* **Error \(with a message\):** Indicates the purge has encountered an error and provides an error message.

