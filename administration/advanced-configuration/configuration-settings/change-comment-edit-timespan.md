# Change comment edit timespan

After posting a comment, a user may want to make changes to it. The user can do this by clicking the three dots on the top right of the comment, and clicking **Edit for 2 min** before the end of the timespan set by this configuration setting. The default timespan is two minutes. After editing and saving a comment, the user will have another timespan during which they can edit the comment.

![](../../../.gitbook/assets/1%20%2874%29.jpg)



Email notifications for comments are not sent until the edit comment timespan has expired. So if the edit comment timespan is set to 30 minutes, the email notification will not be sent until after the 30 minute timespan has expired. If the user edits the comment within that timespan, when the user saves the comment, another 30 minute timespan will start, and the email notification will not be sent until that timespan has expired.  
  
The edit timespan for updates and messages is set using a different setting. To learn more, see [Updates settings](https://community.thoughtfarmer.com/content/106081/updates-settings).

### Set edit comment timespan

1. Go to the **Administration panel**: **Advanced options** section &gt; **Configuration settings** page.
2. Type **comment** in the **Search config settings** field to narrow the config settings results.  ![6.7Admin8883Comment.png](https://community.thoughtfarmer.com/imagethumb/242959230000/16724/305x44/False/6.7Admin8883Comment.png)  
3. Find the config setting comment.edit.timeout.
4. Click in the **Value** column beside the config setting. The default setting is 2.
5. Enter the timespan \(in minutes\) during which users can edit a comment after posting it.
6. Click **Save**.

