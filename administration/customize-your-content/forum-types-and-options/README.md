# Forum types and options

### Forum types and options

When the content type **Forum** is selected while adding or editing a page, a dropdown menu appears on the left with three default forum types available. You can choose the forum type that is most suited to the type of information exchange that you want on that page. You can also [Create custom forum types](create-a-custom-forum-type.md) on the Administration panel.

![](../../../.gitbook/assets/1%20%2861%29.png)



The three default forum types are Discussion, Idea forum, and Q & A \(question and answer\). When you choose a different type of forum, the name of the button used to add a forum post is changed, as follows:

* Discussion: Add topic
* Idea forum: Add idea
* Q & A: Add question

If no specific forum type is chosen, the forum will default to Discussion forum type.  
  
To edit a default or custom forum type, go to the **Administration panel**: **Content** section &gt; **Forum types** page, click the gear icon to the right of the forum type you wish to change, and select **Edit** from the menu that appears.

### Forum sort orders

There are three sort orders available for how you view posts on a forum page: Recent, Popular and A-Z, or alphabetical. Recent and Popular sort options appear on forums by default. A-Z sort appears on forums only if enabled in the Administration panel. The recent sort has the most recently edited posts first. The first posts in the popular sort are determined by a combination of most replies, most likes, and most recent replies.  
  
While you can choose any sort while viewing a forum page, each forum type has a default sort order that can be set from the Administration panel while editing a forum type.

### Enable Alphabetical forum sort

A-Z \(alphabetical\) sort puts forum posts in alphabetical order by post title. A-Z sort only appears on forum pages if enabled in the Administration Panel. To enable A-Z sort:

1. Go to the **Administration panel**: **Advanced options** section &gt; **Configuration settings** page.
2. Type **forum** into the **Search config settings** field to narrow the config settings results.

   ![5.5Admin6199EnableAZSort.png](https://community.thoughtfarmer.com/imagethumb/384874600000/16465/1000x1000/False/5.5Admin6199EnableAZSort.png)

3. Find the config setting forum.tabs.show.alpha.sort.
4. Click in the **Value** column beside the config setting, and set the value to **true**.
5. Click **Save**.

### Forum statistics

Forums have a Card that displays Forum statistics. By default, this Card is found directly below the page header, but it can be moved to any of the columns, or placed below other Cards. The Forum statistics Card shows the number of forum posts, replies, likes, and participants. Profile photos of the most active forum participants within a specified time period also show in the Card. The default time period is 14 days, but the time period can be changed via a configuration setting. If no one has been active in the forum in the specified time period, no profile photos will show.

### Change forum "most active" activity time period

1. Go to the **Administration panel**: **Advanced options** section &gt; **Configuration settings** page.
2. Type **forum** into the **Search config settings** field to narrow the config settings results.

   ![5.5Admin6199EnableAZSort.png](https://community.thoughtfarmer.com/imagethumb/384874600000/16465/1000x1000/False/5.5Admin6199EnableAZSort.png)

3. Find the config setting forum.summary.active.participants.timespan.
4. Click in the **Value** column beside the config setting, and type in the number of days for the forum activity time period.
5. Click **Save**.

### Change number of forum posts per page

If the number of posts added on a forum exceeds the maximum number of posts allowed per page, posts will display on multiple pages within the forum. Arrows at the top of the forum posts allow users to scroll between pages.  
  
To set the number of forum posts allowed per page:

1. Go to the **Administration panel**: **Advanced options** section &gt; **Configuration settings** page.
2. Type **forum** into the **Search config settings** field to narrow the config settings results.

   ![5.5Admin6199EnableAZSort.png](https://community.thoughtfarmer.com/imagethumb/384874600000/16465/1000x1000/False/5.5Admin6199EnableAZSort.png)

3. Find the config setting forum.overview.results.per.page.
4. Click in the **Value** column beside the config setting, and type in the number of forum posts to show per page.
5. Click **Save**.

