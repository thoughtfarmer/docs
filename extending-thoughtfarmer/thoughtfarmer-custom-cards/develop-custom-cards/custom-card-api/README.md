# Custom card API



**On this page:**

* [Adding JSX to page template cards](https://community.thoughtfarmer.com/content/110303/custom-card-api#addingJsx)
* [Dynamically adding cards to a page](https://community.thoughtfarmer.com/content/110303/custom-card-api#Addcard)
* [Global parameters](https://community.thoughtfarmer.com/content/110303/custom-card-api#globalParameters)
* [JavaScript API](https://community.thoughtfarmer.com/content/110303/custom-card-api#jsAPI)

### Adding JSX to page template cards <a id="addingJsx"></a>

Unlike global custom cards, custom cards that are defined in a page template will have their HTML automatically added to the page on render.   
  
If you wish to add JSX to the rendered container instead use the replaceView method. This method is defined in the scope of the cards executing JavaScript code. Its first parameter can be a string of HTML, a DOM Node, or a ReactJS component. It takes a second optional parameter, where you can define the classNames, afterAdded, and beforeRemove options. See [_ctx.customPortlets.add_](https://community.thoughtfarmer.com/content/110303/custom-card-api#addCard) __for more information about these options.  
  
Example usage:

```text
replaceView("A new view", {classNames: 'my-awesome-portlet'})
```

  
**Note:** _replaceView_ is not available to global cards.

### Dynamically adding cards to a page <a id="Addcard"></a>

All global cards run on every page. It is possible to add custom cards to a page template dynamically using the following API. This is helpful for cases when you want to add custom cards under specific conditions. For example, add a custom card to all calendar events on the "HR Calendar".

```text
var page = ctx.customPortlets.getPage();
var currentParentId = page.treePath[page.treePath.length - 1];

if(hrCalendarId === currentParentId){
 ctx.customPortlets.add(<TimeOffRequestForm />,
        {
            placement: tf.portlets.Placement.LaneCenter,
            position: tf.portlets.Position.Top,
            css: portletCss
        });
}
```

It is also possible to use this method to create page template cards that comprise of multiple cards in various locations.

**ctx.customPortlets.add\(view, options\)**

Adds a new card to the current page. The view will be automatically removed when the user navigates to a new page. The simplest usage of this method is:

```text
ctx.customPortlets.add('some <b>html</b> to show');
```

  
First parameter can be either a string, DOM Node, or ReactJS component. By default, all cards are added to the bottom of the right column. If no right column exists, they are added to the center column instead.  
 For greater control, additional options can be passed in using the second parameter. In this example, we specify that the card should be added to the top of the center lane.

```text
ctx.customPortlets.add('<blink>An important message!</blink>', {
    placement: tf.portlets.Placement.LaneCenter,
    position: tf.portlets.Position.Top,
});
```

  
The complete list of available options is:**placement:**    Description: Where the portlet should be displayed. Accessible on the object tf.portlets.Placement    Possible values: LaneLeft, LaneCenter, LaneRight, PageHeader, PageControls, SocialControls, SiteFooter, SiteHeader, ProfileFieldGroups    Default value: LaneRight \(or LaneCenter if LaneRight does not exist\)  
  
Note: SiteHeader is a new addition available in TF 9.1+  
 **position:**    Description: Only applies when the placement value is LaneLeft, LaneCenter, LaneRight, or ProfileFieldGroups    Possible values: tf.portlets.Position.Top, tf.portlets.Position.Bottom, or an integer. Larger integers are further from the top. For profile field groups the integer will indicate the position to insert the custom group.    Default value: Bottom**classNames:**    Description: A string of CSS class names to append to the parent DOM node.  
**label:**  
    Description: Used only for placement ProfileFieldGroups. The label will be the name of the group in the UI.**afterAdded\(node\):**    Description: A callback function that will run once the portlet view has been added to the page  
    Parameters: It receives a single parameter, which the DOM node view was added to.**beforeRemove**\(node\)**:**    Description: A callback function that will run immediately before the portlet view is destroyed. This is a good place to do cleanup.  
    Parameters: It receives a single parameter, which the DOM node view will be removed from.**css:**    Description: A string of CSS that should be added to the page when the portlet view is displayed.**sortOrder:**    Description: A number that is used to determine the visual order of portlets when two or more occupy the same placement value. Lower numbers appear **first:**    Default value: 100**key:**    Description: A unique string used to identify the portlet being added. ctx.customPortlets.remove expects this same value to be passed in.

### Global parameters <a id="globalParameters"></a>

When a custom portlet is executing the following variables are defined in its scope:

* **portletId**: The unique id of the portlet.
* **portletConfig**: The value from the custom portlet editor config field.
* **portletConfigurationId:** A unique Id for this portlet instance. Can be used for storing data.
* **portletCss**: The value from the custom portlet editor CSS field. For page template custom portlets, this is automatically added to the page on render.
* **portletHtml**: The result the server \(C\#\) code defined on this portlet. For page template custom portlets, this value is automatically rendered to the page. Global portlets will need to manually add it using the API methods below.

### JavaScript API <a id="jsAPI"></a>

The following are other methods available for use that will assist in the development of custom cards. For advanced usage please also see [**Integrating with ThoughtFarmer's Flux actions**](https://community.thoughtfarmer.com/content/110305/integrating-with-thoughtfarmers-flux) and [**Communicating between custom cards with events**](https://community.thoughtfarmer.com/content/110304/communicating-between-custom-cards-with).

**ctx.customPortlets.remove\(key\)**

Remove a portlet added through the ctx.customPortlets.add API method. It takes a single parameter, which is a key to identify the portlet.  
  
**Note:** The same key value must have been passed to add on the options object. You do not need to call this unless you want to remove the view before the page changes. All portlets are automatically removed when the page changes.

**ctx.customPortlets.addCss\(key, css\)**

Adds the provided string of CSS globally to the site.  
 **css:**    Description: A string of CSS that should be added to the site.**key:**    Description: A unique string used to identify the CSS being added to avoid duplication. ctx.customPortlets.removeCss expects the same key to be passed in.

**ctx.customPortlets.removeCss\(key\)**

Remove the CSS added through ctx.customPortlet.addCss API method from the site.

**ctx.customPortlets.hasRightLane\(\)**

Returns true if the current page's layout has three columns. There is no hasLeftLane or hasCenterLane methods because they always exist.

**ctx.customPortlets.getUser\(\)**

Returns a plain object containing information about the current user. Example response is:

```text
{
    userId: 1,
    name: 'Bort Simpson',
    firstname: 'Bort',
    culture: 'en',
    profileImageUrl: '/profileimage/34679100000/2217/44x44/True/0,0,0,0/profileimage.jpg',
    isGuest: false,
    inAdminMode: false,
    allowedInAdminMode: true,
    archivedContentEnabled: true,
    securityTokens: [1, 3, 567, 567567],
}
```

**ctx.customPortlets.getPage\(\)**

Returns a plain object containing key properties of the current page. Example response is:

```text
{
    contentId: 1,
    pageType: 1,
    treePath: [1, 2, 3],
    title: 'I am a page',
    tags: [{tagId: 1, name: 'some-tag'}, ...],
    updateDate: '2015-12-23T16:44:50Z',
    publishedDate: '2015-12-23T16:44:50Z'
}
```

**ctx.customPortlets.getUserState\(key, callback\)**

Retrieves data for the currently logged in user previously stored under the given key. The callback receives two props, _key_ and _value_. Value is always a string.

**ctx.customPortlets.setUserState\(key, value\)**

Stores some data server side for the currently logged in user under the given key. Values will be converted to a string when saving.  
  
**Note:** This does not auto serialize objects into JSON. If you want to store an object, you must serialize it first.

**ctx.customPortlets.getData\(portletId, key, callback\)**

Retrieves data previously stored under the given key. The callback receives two parameters, the key and the value.

**ctx.customPortlets.setData\(portletId, key, value, callback\)**

Stores some data server side for the portlet under the given key. Values will be converted to a string when saving. This data is _not_ unique to the current user. The callback receives whether the call failed or succeeded.  
  
**Note**: This does not auto serialize objects into JSON. If you want to store an object, you must serialize it first.

**ctx.customPortlets.findCard\(cardTypeId\)**

Finds the first card in the current page of the specified type. Returns its location in the page structure. The returned data structure looks like:

```text
{placement: 1, position: 4}
```

Is useful for cases where you want to add a new card relative to the position of another card.

**ctx.customPortlets.findAllCards\(cardTypeId\)**

Finds all cards in the current page of the specified type. Returns their location in the page structure. The returned data structure looks like:

```text
[{placement: 1, position: 4}, {placement: 2, position: 1}, ...]
```

**ctx.customPortlets.triggerWebhook\(webhookToken, options, callback\)**

Explicitly triggers a webhook to be sent. _WebhookToken_ is available on the webhooks edit page. It is only available for webhooks using the trigger type "Activity." Options can contain the following values:

* _**contentId**_: The contentId of the page the webhook is being triggered for. **This is required.**
* _**eventName**_: The event that the event is being triggered for. This can be any string value. If it matches an ActivityType, the webhook message is generated as if the activity has just occurred. Example: PublishPage, EditPage. If not specified, this value is defaulted to _custom_. This value is passed along to the webhook destination and can be used to uniquely identify the message.
* _**commentId**_: An optional commentId to associate with the webhook. If eventName equals _AddedComment_, or is a custom value, the comment body is included in the webhook message.
* _**message**_: An additional text value to be included with the webhook body. If the webhook is send Slack messages, this is displayed as the message text.

