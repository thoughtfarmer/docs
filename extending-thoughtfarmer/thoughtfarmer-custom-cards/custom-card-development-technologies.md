# Custom card development technologies

ThoughtFarmer 9 is a .Net Core application. On the back end we use ASP.NET MVC to serve content to the application. The client side portion of ThoughtFarmer was written using React JS and is a single page application. This means that instead of reloading the page for any given click or interaction, the client side portion will call the Web API to get the updated information and React will update only those components that have changed. This results in a much faster web application with greatly enhanced user experience.

### Development technologies

The same mix of technologies that ThoughtFarmer is built on is available when creating custom cards. To allow for dynamic compilation the method for development is slightly different than if you were to develop using an IDE on the desktop. The code for all of these options will go into their proper location in the edit card tool within ThoughtFarmer as shown below. For details please see [Create and edit custom cards.](create-and-edit-custom-cards.md)  
  
The following information will guide you through the technology options available.

#### HTML

Standard HTML can be added to the HTML tab of any custom card. This is great for adding more complex HTML customizations, or generating templates and stubs to be utilized by the JavaScript and CSS portions of the card.

#### JavaScript

ThoughtFarmer cards get sent their content as strings from the server. Once received ThoughtFarmer will run [eval](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/eval) on the JavaScript string content. So keep in mind there is no specific file associated with the JavaScript for a custom card. If you need to debug the script use [debugger](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Statements/debugger) statements within your code to trigger a breakpoint \(this will only be triggered if the dev tools are actually open\).  
  
Getting information from the server is possible with ajax calls to our [REST API ](../thoughtfarmer-rest-api.md)or by using the [JavaScript API](develop-custom-cards/custom-card-api/)available. 

#### ReactJS

ThoughtFarmer utilizes ReactJS. This means you can also code custom cards using React components. JSX templates are a powerful new tool that allow you to build components quickly and intuitively.  
  
JSX is supported directly within the custom cards JavaScript area. ThoughtFarmer 9.0+ will transpile all jsx within custom cards into proper JavaScript for execution within the application. There is no need to use external tools to do this. 

#### CSS and SCSS

In order to style your custom cards you can use the CSS area to add any style information you need. Keep in mind that [Sass](https://sass-lang.com/) is also supported in this area. All content entered here will be transpiled from scss to proper css for use by your custom cards within the application.  


