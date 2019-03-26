# Integrating with ThoughtFarmer's Flux actions

The custom card JavaScript API has an interface for listening to, and create Flux actions. This allows custom cards to create quick flux "stores" with minimal code.  
 **Warning:** Custom cards should favour the [event listener API](communicating-between-custom-cards-with-events.md) instead of listening to actions. Actions are useful when you need to tie into, or extend core functionality. An example of this is performing an action when a user joins a group \(e.g. tf.core.AppActions.JoinGroup\)  
  
Code that is dependent on these core actions will be brittle and may break on upgrade. For a list of current actions for your ThoughtFarmer version you can create a request at [helpdesk@thoughtfarmer.com](mailto:helpdesk@thoughtfarmer.com).  

**addActionListener\(callback: function\);**

Adds a callback function that will be called for every action that occurs in ThoughtFarmer. This function returns an ID value that you need to retain for un-registering your listener.

**removeActionListener\(id\);**

Removes your listener from the flux app dispatcher. _Id_ is the value returned from calling _addActionListener._

**dispatchAction\(action: string, data: any\);**

Dispatches a flux action across the application.

* **Action** is an enum like string value defined on _tf.core.AppActions._ 
* **Data** is any object that you want to pass through with the action. It can be omitted.

  
Be careful firing actions, these are core code and subject to change in the future. There are few use cases where this is necessary. Favour the [event listener API](https://community.thoughtfarmer.com/content/110304/communicating-between-custom-cards-with) instead for communicating between custom cards.

**Example**

```text
// called for every action that occurs in the application. Check the type, and handle.
function onAppAction(payload) {
  var action = payload.action;
  var data = payload.data;
  
  switch(action) {
    case tf.core.AppActions.JoinGroup:
      console.log('The user joined the group');
      break;
    case tf.core.AppActions.LeaveGroup:
      console.log('The user left the group');
      break;
  }
}

// add the listener
var actionListenerId = ctx.customPortlets.addActionListener(onAppAction);

// add our view.
replaceView(<p>example card</p>, {
    beforeRemove: () => {
        // always clean up your listeners
        ctx.customPortlets.removeActionListener(actionListenerId);
    }
});
```

