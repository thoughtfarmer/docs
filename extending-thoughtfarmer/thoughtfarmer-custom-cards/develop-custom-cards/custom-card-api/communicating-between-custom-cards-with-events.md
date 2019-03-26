# Communicating between custom cards with events

The custom card JavaScript API has an interface for listening to, and creating events for communication. This allows custom cards to implement more flux-like patterns. This allows async operations \(such as data loading\) to be separated from the views, and custom React components that properly add/remove event listeners can avoid the need for _isMounted_ checks. This API can also be leveraged for communication between different custom cards.

**addEventListener\(type: string, callback: function\);**

You can add an event listener using the addEventListener method.  
  
**type** __is a string, it does not have to be defined anywhere beforehand. You can add as many listeners for the same type as you need. It is a good practice to make the type value fairly unique to avoid potential collisions. For example, prefer _'tfc-required-reading-update'_ over a more generic value like _'update'_.  
  
**callback** is a function you want to be called when the event is fired.  
  
**NOTE:** Make sure to remove any listeners when the custom card is destroyed.  
 

**removeEventListener\(type: string, callback: function\);**

The values for this method are the same as _addEventListener_. It is safe to call even if _addEventListener_ was not previously called.  
 

**fireEvent\(type: string, arg1: any, arg2: any, arg3: any\);**

Fires an event to all listeners added through the addEventListener method.   
  
**type** __is the name of the event you are firing. Unlike flux actions, only listeners for the specific event type are called.  
  
**arg1, arg2, arg3** are values you want to pass to the listener. You do not need any arguments, 3 is the maximum.  
 

**Example**

```text
var SearchResultsEventName = 'tfc-sweet-search-results';

function createSearchAction(searchQuery) {
    tf.api.newApiRequest('/api/search', searchQuery, 'POST', function (resp) {
        ctx.customPortlets.fireEvent(SearchResultsEventName, resp.success, resp.data);
    });
}

class TFC_SweetSearchResults extends React.Component {
    constructor(props) {
        super(props);

        this.state = {
            isLoading: true,
            hasError: false,
            results: [],
        };

        this.onSearchResults = this.onSearchResults.bind(this);
    }
    componentDidMount() {
        this.props.ctx.customPortlets.addEventListener(SearchResultsEventName, this.onSearchResults);

        createSearchAction({ query: 'test' });
    }
    componentWillUnmount() {
        this.props.ctx.customPortlets.removeEventListener(SearchResultsEventName, this.onSearchResults);
    }
    onSearchResults(success, data) {
        if (!success) {
            this.setState({ isLoading: false, hasError: true });
            return;
        }

        this.setState({ isLoading: false, results: data.items });
    }
    render() {
        if (this.state.isLoading) {
            return <div>Loading...</div>
        }

        return <div>{`There were ${this.state.results.length} search results found`}</div>
    }
}

replaceView(<TFC_SweetSearchResults ctx={ctx} />);
```

