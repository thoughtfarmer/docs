# Create and edit custom cards

**Go to**:

* [Manage cards administration page](create-and-edit-custom-cards.md)
* [Import a card](create-and-edit-custom-cards.md)
* [Create a card](create-and-edit-custom-cards.md)
* [Edit a card](create-and-edit-custom-cards.md)
* [Export a card](create-and-edit-custom-cards.md)
* [Upgrade a card](create-and-edit-custom-cards.md)
* [Global cards](create-and-edit-custom-cards.md)

## Manage cards administration page

The first step in creating or editing a ThoughtFarmer custom card is to navigate to the **Admin panel**: **User interface** section &gt; **Cards** page.  
  
The tables on the **Cards** page are your card and sub-application library. This shows every customization that is available on your intranet. These are separated out into 4 categories:

1. **Page template cards**
   * Cards that are added individually to a page or template. Most cards will end up here.
2. **Page template applications\***
   * Sub-applications that are added individually to a page or template
3. **Global cards**
   * Cards that run on every page of the intranet
4. **Global applications\***
   * Sub-applications that run on every page of the intranet

\*A note on custom applications: These features are currently in beta. If you are interested in writing a sub-app, please contact the [ThoughtFarmer helpdesk](https://thoughtfarmer.zendesk.com/). The information below explains how to manage your custom cards.  
  
Each table contains the following information about each card:

* **Id:** A unique card id is automatically generated when you create a card. This is the id you use to push a card you are working on locally to your Intranet using the [custom dev tools](https://community.thoughtfarmer.com/content/106244/custom-card-dev-tools).
* **Name:** The name of the card. If the card has a description, an info icon appears that you can click to display that information. You can also click the name to edit the code for the card.
* **Layout Usage:** For page template cards and apps, this indicates the number of page templates the card is applied on. If one or more, clicking on the number will bring up a modal with the linked name of page\(s\) it is being used on. 
* **Page Usage:** For page template cards and apps, this indicates the number of unique pages the card is applied on. If one or more, clicking on the number will bring up a modal with the linked name of page\(s\) it is being used on.
* **Modified by:** Indicates who last modified this card.
* **Date modified:** Indicates when the card was last modified.
* **Viewable by**: When "Admins only" is checked it indicates the card is only able to be added to templates by admin users. Otherwise, anyone with edit permissions to pages may utilize the card.
* **Active**: When active, this card will be available to be added to pages and all current instances will render. Deactivating a card will make it unavailable to add to pages. Any current templates using that card will also be set to inactive and not display.
* **Action:** Click the **gear icon** to open a menu with the actions below.
  * **Edit card:** Takes you to the template editor to change the code for the card.
  * **Export card:** Allows you to export the template to a zip file.
  * **Replace card:** Allows you to import upgrading version or replacement for the current card. 
  * **Delete:** Removes the card from the intranet including all instances currently added to page templates. NOTE: You cannot delete an active card. It must be deactivated first.

![](../../.gitbook/assets/1%20%2831%29.png)

## Import a card

Cards can be imported into your intranet. When you click on the **Import card** button at the top right of the page, a dialog will appear asking you to select the zip file containing the card to import. After selecting the zip file and clicking ok, the card will be imported and appear in  either the page template cards table or global cards table. The card automatically 'knows' what type it is depending on what it was originally created as.

## Create a new card

Clicking the blue **+** **Create page template card** button at the bottom right of each table will take you to the custom card editor screen. This screen has a number of tabs and fields that allow you to modify the page template card. Learn more about your options below, or go to [ThoughtFarmer development technologies](develop-custom-cards/thoughtfarmer-developer-tools/) for more information.

![](../../.gitbook/assets/2%20%2824%29.png)



* **Card name:** The name of the card.
* **Template Id:** The unique card id
* **Markup\(HTML\)\*:** This is the tab where any standard HTML is entered and is what the user sees when the card is run. \(eg. Image tags, links, etc.\)
* **Client \(JavaScript\):** This is the tab where any JavaScript code that the card requires is entered. ThoughtFarmer 9 is built on React and we support React components here. Any React written here is automatically run through babel. You can also write plain JavaScript and jQuery. 
* **Styling \(CSS\):** This is the tab where any CSS styling used by the card is entered. If you prefer, you can also write SASS directly in this tab, which will also be compiled on Save.
* **Preview:** The **Preview** tab allows you to run the card and see how it currently looks. You can change various **Preview settings**, and then click **Refresh** to reload the preview tab.
  * **Preview content id:** This is the content id that will be passed into the preview card. This is useful if your card is only intended to appear on certain pages.
  * **Preview user:** This is the user the preview will be run as. This is useful if your card is intended to be viewed by only certain users.
  * **Configure card:** This is the configuration information that you can pass into the preview instance of the card as a JSON object. This is useful if your card depends on any configuration before it runs. If needed, this will match the format of your default configuration in the details tab.
* **Details:**
  * **Description:** This is a description of what the card does. It will show in the **Manage cards** admin page when the user hovers over the \(i\) icon inline with the card title.
  * **Default configuration:** If there is information that you need to pass into the card when it is run, that goes here. The configuration must be in the [JSON](http://json.org/) object format.
    * ```text
      Eg.{ "customTitle": "The best page!", "adminsOnly": false }
      ```
  * **Allow card configuration on edit page:** If your card has per instance configuration, then this setting will allow for this to be configured separately for each instance when it is added to page template.
  * **More information:** This is a URL to a page with more information about this card.

Click **Save** when you finish creating the card.  
  
\*You might remember that this tab used to be for CSHTML. This has now been deprecated.

## Edit an existing card

Click the **gear icon** in the far right column in the row for the card you want to edit, and select **Edit card** from the menu that opens to go to the custom card editor screen.  Also, if you click on the name of the card you will be brought straight to the editor. This screen has a number of fields that allow you to modify the page template card.  
  
The available fields on this page are the same as those described above under the **Create a new card** heading, with the addition of one field:

* **Version:** A dropdown from which you can ****access a history of past changes made to the card, who made them, and when. Choosing an item from this drop-down reloads the page to show a read-only view of this version. To revert to this version, click the **Revert** button. Otherwise, click **Cancel** to return to the most recent version of the card.

Click **Save** when you are finished editing the card\*\*.  
  
\*\*NOTE: If you save a new version of a card and there are existing templates that have the card added, you will see a green banner at the top saying "{My Custom} card has been edited. You may want to upgrade the card {My Custom}. Or you can **upgrade now**." Clicking "upgrade now" will push the update to all cards that are active on page templates.

## Export an existing card

To make use of a card on another ThoughtFarmer installation, or to archive it outside of the application, you can export the card directly from the **Manage cards** page. In the **Administration Panel**: **User interface** section &gt; **Manage cards** page, click on the gear icon to the right of the desired card. In the dropdown menu that opens, click **Export card** and save the generated zip file in the desired location on disk.

## Upgrade your card with a new version

It is now easy to upgrade a card with an external zip file without any copy/pasting. It will be automatically added to all the page templates you have previously selected. Click the gear icon beside the card you wish to upgrade and click 'Replace custom card'. This will bring up a modal where you can browse to your desired .zip file and upload it.

## Global cards

Global cards have the same C\#, JavaScript, and CSS components as their page template counterparts. However, the code for these cards will be set to run globally and to bypass all per page template configuration. There is a special [JavaScript API](develop-custom-cards/custom-card-api/) for placement of global cards on pages.

