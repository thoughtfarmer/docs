# Delete users



### How to delete user accounts

Deleting a user means that the user's profile will be completely removed from ThoughtFarmer. Since every piece of content is owned by a user, _before_ deleting a user, all that user's content must have its ownership changed, and be moved out from under the user's profile page, or it must be deleted.

### Part 1: Change ownership of a user's content

#### Find all content owned by a user

1.Go to the **Administration panel**: **Content** section &gt; **Change owner** page.

2.Start typing the name of the current owner in the **Current owner** box.

![](../../.gitbook/assets/1%20%2828%29.png)

3.Click once on the current owner from the list that drops down.

4.Click the **Find content** button.

#### Select content to be changed to new owner

After following the four steps above, all content for the current owner will display in two ways. On the left, an expandable tree navigation of the site directory shows the pages owned divided into the main sections of the intranet. On the right, you can scroll through a list of all the user's pages that are selected for changing ownership.

1.To change ownership of all of the user's pages to one owner, skip to **Step 4** \(as all the user's pages are selected by default\).

2.To change ownership of the user's pages to multiple owners, follow the steps below for one new owner at a time, then repeat for the other new owners. First, uncheck the box at the top left.

![](../../.gitbook/assets/2%20%2857%29.jpg)

3.Navigate through the directory of pages by clicking on the rotating triangles on the left. Select only the pages or sections of pages whose ownership you wish to change. Hover over sections to see a pop-up telling you how many subpages the user owns in that section. The list on the right will automatically refresh showing only the pages that are selected.

![](../../.gitbook/assets/3%20%2828%29.jpg)

1. When you have selected the desired pages, start typing the name of the new owner in the **New owner**box at the bottom.
2. Click once on the new owner from the list that drops down.
3. Click **Change owner** to change ownership of the selected pages. The page will refresh showing the message: You have changed \(\#\) of \(Current owner's\) items to be owned by \(New owner\).

#### Part 2: Delete user

1.Go to the ThoughtFarmer **Administration Panel**: **Users & security** section &gt; **User management** page.

2.Use the filter, sort, and query tools to find the desired user or set of users \(see [Find users](find-users.md) for more info\).

![](../../.gitbook/assets/4%20%2816%29.png)

3.Select the checkbox beside the desired user\(s\) you wish to delete.

4.In the "Choose an action..." dropdown select **Delete user**.

5.Click **Go.**

6.Click **OK** in the pop-up to confirm the deletion.

_For AD users;_ if [automatic user creation](../activity-directory-integration/active-directory-basic-settings/) is enabled, then the user's AD account must be inactive, deleted or removed from the synced-to AD group configured on the Employee Directory Connector page. Otherwise, the user's profile page will be recreated during one of the automatic creation processes, or if the user tries to log in again.

