# Set up a goal



Goals can be tracked in Piwik based on specific actions by users in ThoughtFarmer. When users complete these actions they are tracked as a "Conversion" in Piwik.  
  
Goals in Piwik are anonymous and so should be used to track frequency of goal completion, rather than which specific users have completed a certain goal.  
 

#### Goal triggers <a id="section1"></a>

Piwik comes with 4 visitor triggers that can be configured when creating a goal. Additionally, you can use javascript to trigger a manual goal. Please see the [custom goals](custom-goals.md) page for more information.  
  
The 4 Piwik default triggers are:  
  
**Visit a given URL:** The criteria for the goal is determined by the URL of a page or group of pages.  
**Visit a given Page Title:** The criteria for the goal is based on the format of the actual ThoughtFarmer page title.  
**Download a file:** The goal is based on when a user downloads a file or group of files.  
**Click on a Link to an external website:** To track when users exit ThoughtFarmer to a specific site for a link or collection of links.  
  
Matching criteria for the 4 above can be either **contains**, **is exactly**, or **matches the expression**. Examples for matching patterns can be found directly in the user interface when creating the goal.  
 

#### Create a goal <a id="section2"></a>

To create a goal just keep in mind the type of trigger you want to use \(as outlined above\). Then use the following steps:

1. Click the **Goals** tab in Piwik.
2. Scroll down to the Goals management section and click **Create a new Goal.**
3. Enter a **Goal Name.**
4. In the **Goal is triggered** section select **when visitors.**
5. Select one of the 4 triggers in the **Goal is triggered** section.
6. Select a match criteria in the **where the** _**XYZ**_ section \(XYZ will switch according your selection in \#5 above\).
7. Decide if the goal can be converted once a visit or not and configure **Allow multiple goals per visit.**
8. Click **Add Goal.**

#### Example goals <a id="section3"></a>

  
**Edit profile goal \(for ThoughtFarmer 5.0 and up\):**

1. Click the **Goals** tab in Piwik.
2. Scroll down to Goals management section and click **Create a new Goal.**
3. Enter a **Goal Name** \(e.g. "Edit profile"\)
4. In the **Goal is triggered** section select **when visitors.**
5. Select **Visit a given URL** in the **Goal is triggered** section.
6. Select **where Page Title** --&gt; **contains** --&gt; and enter the text "**profile/edit".**
   * ![contains+profile+edit.png](https://community.thoughtfarmer.com/imagethumb/144445630000/16390/1000x1000/False/contains+profile+edit.png)
7. Select **Goal can only be converted once per visit** \(to avoid multiple conversions for frequent edits\).
8. Click **Add Goal.**

  
**Visit a specific page:**

1. Click the **Goals** tab in Piwik.
2. Scroll down to the Goals management section and click **Create a new Goal.**
3. Enter a **Goal Name** \(e.g. "View CEO Blog page"\)
4. In the **Goal is triggered** section select **when visitors.**
5. Select **Visit a given URL** in the **Goal is triggered** section.
6. Select **where Page Title** --&gt; **contains** --&gt; ande enter the text "**/content/XYZ**" \(replace XYZ with the contnent ID of the desired page\).
   * ![content+goal.png](https://community.thoughtfarmer.com/imagethumb/142983270000/16391/1000x1000/False/content+goal.png)
7. Select **Goal can only be converted once per visit.**
8. Click **Add Goal.**

