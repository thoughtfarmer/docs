# Deferred javaScript loading

In order to improve browser responsiveness and client side performance we have added a configuration setting to defer the loading of all JavaScript .   
  
When the configuration setting javascript.deferredLoading is set to _true_, all JavaScript is loaded and executed after the web page has rendered. As a result, custom JavaScript added to ThoughtFarmer should follow the deferred pattern.

ThoughtFarmer defines two global JavaScript functions, _onReady_ and _onAppReady_, that can be used to write deferred loading compatible JavaScript. Both onReady and onAppReady take a single function as a parameter that will be executed at a later point in time. Functions passed to onReady will be called after the first page render, and functions passed to onAppReady will be called after all external JavaScript files have been loaded.

ThoughtFarmer defines a third global function called addScript which can be used to add external JavaScript files to the page. addScript should only be called in an onReady callback or it may interfere with page load performance and JavaScript execution order.

Examples:

```text
<script>

onReady(function() { 
     // add a new script to the page 
     addScript("/path/to/file.js"); 

     // You can do other JavaScript here, as long as it doesn't depend on 
     // any other external JS, as it may not be available yet. 

});

onAppReady(function(){ 
     // jQuery and any script added using addScript() are now available. 

});
</script>
```

