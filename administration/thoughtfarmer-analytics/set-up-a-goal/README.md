# Set up a goal

Goals can be tracked in ThoughtFarmer Analytics based on specific actions by users in ThoughtFarmer. When users complete these actions they are tracked as a "Conversion".  
  
Goals in ThoughtFarmer Analytics are anonymous and so should be used to track frequency of goal completion, rather than which specific users have completed a certain goal.

### Goal triggers <a id="section1"></a>

ThoughtFarmer Analytics comes with 4 visitor triggers that can be configured when creating a goal.  
  
The 5 default triggers are:

* **Visit a given URL:** The criteria for the goal is determined by the URL of a page or group of pages.
* **Visit a given Page Title:** The criteria for the goal is based on the format of the actual ThoughtFarmer page title.
* **Send an event:** The criteria for the goal is based on a event trigger on a ThoughtFarmer page \(supported events: page create, edit, comment\).
* **Download a file:** The goal is based on when a user downloads a file or group of files.
* **Click on a link to an external website:** To track when users exit ThoughtFarmer to a specific site for a link or collection of links.

Matching criteria for the 5 above can be either **contains**, **is exactly**, or **matches the expression**. Examples for matching patterns can be found directly in the user interface when creating the goal.

### Create a goal <a id="section2"></a>

To create a goal just keep in mind the type of trigger you want to use \(as outlined above\). Then use the following steps:

1. Click the **Goals** tab on the left hand side menu.
2. Click **Add a new Goal.**
3. Enter a **Goal Name.**
4. In the **Goal is triggered** section select **when visitors.**
5. Select one of the 5 triggers in the **Goal is triggered** section.
6. Select a match criteria in the **where the XYZ** section \(XYZ will switch according your selection in \#5 above\).
7. Decide if the goal can be converted once a visit or not and configure **Allow multiple goals per visit.**
8. Select a **Goal Revenue** if applicable \(For example: a Form submitted by a visitor may be worth $10 on average. ThoughtFarmer Analytics will help you understand how well your visitors segments are performing\).
9. Click **Add Goal.**

### Example goals <a id="section3"></a>

**Edit profile goal:**

1. Click the **Goals** tab on the left hand side menu.
2. Click **Add a new Goal.**
3. Enter a **Goal Name** \(e.g. "Edit profile"\)
4. In the **Goal is triggered** section, select **when visitors**.
5. Select **Visit a given URL** in the **Goal is triggered** section.
6. Select **where Page Title** --&gt; **contains** --&gt; and enter the text "**profile/edit".**
7. Select **Goal can only be converted once per visit** \(to avoid multiple conversions for frequent edits\).
8. Click **Add Goal.**

**Visit a specific page:**

1. Click the **Goals** tab on the left hand side menu.
2. Scroll down to the Goals management section and click **Create a new Goal.**
3. Enter a **Goal Name** \(e.g. "View CEO Blog page"\)
4. In the **Goal is triggered** section, select **when visitors.**
5. Select **Visit a given URL** in the **Goal is triggered** section.
6. Select **where Page Title** --&gt; **contains** --&gt; and enter the text "**/content/XYZ**" \(replace XYZ with the content ID of the desired page\).
7. Select **Goal can only be converted once per visit.**
8. Click **Add Goal.**

