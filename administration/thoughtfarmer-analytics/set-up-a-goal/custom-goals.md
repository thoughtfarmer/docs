# Custom goals

It is possible to track goals that cannot be created by the ThoughtFarmer analytics default options. You can create custom javascript that will trigger this goal to be tracked. You can then apply this script to any javascript triggerable event. For example:

* Time on page \(e.g. to track if users viewed an embedded video\)
* Liked a page
* Updated their status
* Favourited a page

####  Update status custom script example

This example will go through all the steps required to create a custom goal that will track when an user updates their status.   
  
**First you need to create a manual goal:**

1. Click the **Goals** tab.
2. Click **Add a new Goal.**
3. Enter a **Goal Name** and **Description**.
4. In the **Goal is triggered** section select **manually.**
5. Select **Allow Goal to be converted more than once per visit** \(may vary depending on your use case\).
6. Click **Add Goal.**
7. Go back to Goals tab, click on **Manage Goals**.
8. Get the numerical **Id** from the first column for the newly created goal.

  
**Add the custom script:**  
In ThoughtFarmer go to the **Administration Panel**: **User interface** section &gt; **Create Cards**  &gt; **Create a Global Card** &gt; **Client \(Javscript\)** tab. Insert the following code in the textarea:

```text
<script type="text/javascript">

(function($) {

 $('#statusInput, #status-input').bind('keypress', function(event) {
    if(event.keyCode == 13) {
       if(Piwik !== undefined) {
          var pageProperties = $.pageProperties();
          piwikTracker = Piwik.getTracker(pageProperties.stats.url + 'piwik.php', pageProperties.stats.siteId); 
          piwikTracker.setUserId(pageProperties.user.userName);
          piwikTracker.setCustomDimensions({'dimension1': pageProperties.user.fullName});
          piwikTracker.trackGoal(2);
```

```text
       }
     }
 });

})(jQuery);
</script>
```

  
Modify the line above and replace the numerical value with the Id for that goal you collected from the previous step.

```text
piwikTracker.trackGoal(X);
```

You won't be able to see data for the goal right away. However you can test to ensure this is working by triggering the goal in ThoughtFarmer. Then log in to the TF Analytics dashboard. You should see a green conversion icon show up for your user account. Hover over the icon and ensure the title is associated with the goal you just created.  


