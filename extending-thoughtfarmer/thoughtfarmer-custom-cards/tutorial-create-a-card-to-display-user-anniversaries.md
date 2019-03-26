# Tutorial-create a card to display user anniversaries

This tutorial is intended to show you the principles of the code involved to create \(and potentially extend\) a custom card using data fetched from the ThoughtFarmer public API. Please note: **TF version 9** or higher is required.In this example, we are going to walk through the creation of a card that will display users' 1-year and 5-year work anniversaries for the current month. You'll be able to display the card on any column on the site. The user's name, when clicked, will take you to their profile.  
  
The image below shows the finished product; the two possible states of our custom card:  
  
![anniversaries.png](https://community.thoughtfarmer.com/imagethumb/217687030000/14344/298x301/False/anniversaries.png)   -OR-   ![workannis\_none.png](https://community.thoughtfarmer.com/imagethumb/18985130000/14345/299x171/False/workannis_none.png)  
  
First off, navigate to **Administration panel** &gt; **Content** &gt; **Profile details,** and ****set up a **custom date field** called 'Anniversaries'. Go to some user profiles and fill this field out. This is the data we are going to fetch and display! Now let's begin.

### Navigate to the custom card authoring screen

Go to the **Administration panel** &gt; **User interface** section &gt; Manage cards page. On that page click the **Create page template card** button.  
The first thing to do is to give the card a **name**, let's go with "Work Anniversaries". Hit **Save**.

### Add code to the card editor

**Step 1: Configure your card**

Now, let's set up some custom configuration for your card. The configuration object allows you to easily tweak how your card looks. This information will be passed into the React component we will build out for our card. Hit the **details** tab and in the **Default configuration** text area, add your configuration code:

```text
{ 
"customFieldName": "Anniversary",
"title": "Work Anniversaries", 
"noResultsMessage": "There are no anniversaries this month", 
"yearsToShow": ["1", "5"], 
"iconClass":"fa-star" 
}
```

Using this configuration object will make it easy to go back and make changes to, for example, which anniversary years you want to show. If you wanted to show 10 year work anniversaries as well, you could change the "yearsToShow" to:

```text
"yearsToShow": ["1", "5", "10"], 
```

Next, head to the **Client \(JavaScript\)** tab. We are going to add some code. First, we need to tell our card to grab and parse the configuration settings we just set in that details panel from portletConfig. \(Portlet is another word for card.\) The most important line in the code below is  config = JSON.parse\(portletConfig\);. This is what actually does the grabbing and the parsing, the rest of the code is setting fallbacks if nothing is set in the configuration panel.

```text
var config = {};

try {
    config = JSON.parse(portletConfig);
    if (!config) {
        config = {};
    }
} catch (err) {
    config = {};
}

if (!('customFieldName' in config)) {
    config.customFieldName = 'Anniversary';
}
if (!('showNumberOfYears' in config)) {
    config.showNumberOfYears = true;
}
if (!('yearsToShow' in config)) {
    config.yearsToShow = [];
}
if (!('iconClass' in config)) {
    config.iconClass = 'fa-star-o';
}
```

**Step 2: API call to get that data**

Next lets start setting up our React component. This will act as our skeleton to support the API call we are going to make to the API endpoint that contains the anniversary dates.  
 

**SIDEBAR: ABOUT THE THOUGHTFARMER API**

You can find documentation that describes all the API calls you can make, customized to your Intranets API, by going to [http://YOURINTRANETNAME/admin/api.](http://yourintranetname/admin/api.) You can do tests to see what data you can get back by clicking on the different API calls you can make and in the top right corner, clicking 'Try it Out', followed by the big blue 'Execute' button. All this data is available to you to harness and display in your custom cards.  
  
To look at the raw user data available to you, I suggest going to http://YOURINTRANETNAME/api/users and check out the JSON object you can get back in your browser.  
  
But wait! Where is our anniversary data? Because the 'Anniversary' field for user profiles _is a custom field_, we need to specify that we want that extra data back. If you don't have a field for this you can add one using the **Administration Panel** &gt; **Content** section &gt; **Profile details** page.   
  
Try, http://YOURINTRANETNAME/api/users/?extraFields=anniversary.  Anniversary data will be nested inside the customFields key of your user object.  
  
To get more custom fields back, you can append the field names onto this query like this:  
http://YOURINTRANETNAME/api/users/?extraFields=anniversary,yourdogsanniversary,favouritefood,whatevercustomfieldyouwant

  
In this case, we are going to first be _searching_ for users that have an anniversary in the current month.  
  
We don't want to get all our intranet's users back - in this use case, the users that don't have anniveraries set, or that don't have anniversaries in the current month, are useless to us. So, we will first use  /api/search/users to filter those users out from the beginning.  
  
Back to the code:

```text
class TFC_WorkAnniversaries extends React.Component {

    constructor(props) {
        super(props);
        this._isMounted = false;

        this.state = {
            isLoading: true,
            hasError: false,
        };
    }
    //Highlighted in  orange is the API call we will use to get back users by ID that have work anniversaries this month. 
    // All API calls should go within a componentDidMount() function.
    componentDidMount() {
        //first get the name of custom field we are searching from the config 
        var customFieldName = this.props.customFieldName; // 'Anniversary'

        //next is a bit of work done before the call to construct search request body. 
        // Notice in your API docs /api/search/users section, there is a "forCustomFieldDates" object within the data 
        // you receive back from this endpoint with "additionalProp1" , which in this case is our "anniversary" field. 
        // We are looking to grab anniversaries happening this month, so we will pass this month in as the value. 
        var forCustomFieldDates = {};
        forCustomFieldDates[customFieldName] = {
            month: (new Date().getMonth() + 1)
        };
     //pass in those extra parameters we just set out above to the API call
        tf.api.newApiRequest('/api/search/users', { forCustomFieldDates }, 'POST', function (resppnse) {
           //check for response
            if (resp.status !== 200 || (resp.data && resp.data.items && resp.data.items.length === 0)) {
                this.setState({ isLoading: false });
                return;
            }
             //I suggest console.log(response.data);'ing here to see the whole object you get back

            //next grab the user IDs of users that have a work anniversary this month from our response.data.items
            var userIds = response.data.items.map(function (u) {
                return u.userId;
            });

            //Our 2nd API call will load users from results of our previous one by user ID, including the custom anniversary field
            tf.api.newApiRequest(`/api/users?userIds=${userIds.join(',')}&extraFields=${customFieldName}`, function (resp) {
                if (resp.status !== 200) {
                    this.setState({ isLoading: false });
                    return;
                }
                //console.log(resp.data); again to see our users work anniversaries for this month
            });
        });
    }

    render(){
        return(
          <div>Nothing to render yet!</div>
        );
    }

}

//Highlighted in green is where we are passing our configuration settings set in the panel
// as a property to our React component. 
replaceView(<TFC_WorkAnniversaries 
              customFieldName={config.customFieldName} 
              yearsToShow={config.yearsToShow}
              noResults={config.noResultsMessage}
              iconClass={config.iconClass}
            />);
```

**Step 3: Organize your data**

Now we will organize our data to make our job easier later on when we want to render these work anniversaries. Note that this code is still enclosed within the context of the 2nd API request:

```text
          tf.api.newApiRequest(`/api/users?userIds=${userIds.join(',')}&extraFields=${customFieldName}`, function (resp) { 
                    if (resp.status !== 200) { 
                        this.setState({ isLoading: false }); 
                        return; 
                 }

                var results = resp.data;
                var usersByYear = {};
                var thisYear = new Date().getFullYear();

                // loop over the results to construct your 'usersByYear' object - 
                // our users with anniversaries this month will be grouped by year in this format:
                // usersByYear = {1:[{userA},{userD}...],5:[{userA},{userB]};
                // You can add a debugger; here to step through the how the object is created
                for (var i = 0; i < results.length; i++) {
                    //get first user from resp.data 
                    var result = results[i];
                    result.anniversary = moment(this.getCustomFieldValue(result, customFieldName));
                    result.numYearsSince = (thisYear - result.anniversary.year());

                    if (result.numYearsSince > 0) {
                        //if there already an array within this usersByYear object with the anniversary year key, push in this user obj
                        if (`${result.numYearsSince}` in usersByYear) {
                            usersByYear[`${result.numYearsSince}`].push(result);
                        // else create the array with the result in it
                        } else {
                            usersByYear[`${result.numYearsSince}`] = [result];
                        }
                    }
                }
                 //console.log to see your usersByYear object!!!
                // add the usersByYear obj to the state so we can access it in our render() next
                this.setState({
                    usersByYear,
                    isLoading: false
                });
             });
```

Outside of componentWillMount\(\), we will use a helper function with Moment.js to format our anniversary date. We are passing in the user object and the custom field you want to isolate the data from as arguments.

```text
 getCustomFieldValue(result, customFieldName) {
        var val = null;
        //loop in case there are multiple custom fields. This will only go once since were getting 1 field.
        for (var i = 0; i < result.customFields.length; i++) {
            var customField = result.customFields[i];
             //get the custom field value and return up to result.anniversary
            for (var j = 0; j < customField.label.length; j++) {
                //check your getting the correct field value
                if (customField.label[j].value === customFieldName) {
                    return customField.value;
                }
            }
        }

        return val;
    }
```

TL;DR  
Let's review:

1. We set up our React parent component, and first got the User ID's of people with work anniversaries this month.
2. We then got the anniversary data for all those users, and sorted them by year into an object called usersByYear.
3. Each user with a 1 or 5 year anniversary was placed into an array within usersByYear object. Each user within each year array is its own nested object.

Now, lets get to work at actually rendering that data.

**Step 4: Render the data**

Below is our render function, the final function in our TCF\_AnniversaryCard component. Read through the comments and copy this into your code.

```text
 render() {
        var view = null;
        if (this.state.isLoading) {
            view = <div className="tfc-anniversary-view"><LoadingIndicator /></div>;
        } else {
            //get yearsToShow & noResults msg from your config, passed into your component with replaceView() above.
            var yearsToShow = this.props.yearsToShow;
            var noAnniversaries = this.props.noResults;
            //get usersByYear object from state
            var usersByYear = this.state.usersByYear;

            //initialize rows array
            var rows = [];
            //get years we are targeting, make sure they go biggest -> smallest
            // map over year.
            //our child components below will take care of the rest of the rendering
            Object.keys(usersByYear).sort().reverse().map(function (year) {  // year = 1, year = 5

                if (yearsToShow.length === 0 || yearsToShow.indexOf(year) > -1) {
                    rows.push(<TFC_AnniversaryYear key={year} year={year} users={usersByYear[year]} />);
                }

            });

            if (rows.length > 0) {
                view = <div className="tfc-anniversary-view">{rows}</div>;
            } else {
                view = <div className="tfc-anniversary-view">{noAnniversaries}</div>;
            }
        }

        return <div className="tfc-portlet-anniversary tfc-anniversary">
            <h1 className="tf-portlet-heading">
                <span className="tf-inner-text">{anniversaries}</span>
                <i className={`tf-portlet-icon fa ${this.props.iconClass}`} />
            </h1>
            {view}
        </div>;
 }
```

b   = here we are passing our year info and usersByYear info down to our child component as props. Since we are using map\(\) we need a key or React will throw an error.  
  
Note the necessary props are destructured and passed into these child components. 

```text
 const TFC_AnniversaryYear = ({ year, users }) => {
    var userItems = users.map((user) => {
        return <li key={user.userId} className="tfc-anniversary-item"><TFC_AnniversaryUser user={user} /></li>;
    });

    return <div className="tfc-anniversary-user-list">
        <h4 className="tf-portlet-subheading tfc-anniversary-year">{year} {(year === '1') ? year : years}</h4>
        <ul className="tfc-anniversary-list">
            {userItems}
        </ul>
    </div>;
};

const TFC_AnniversaryUser = ({ user }) => {
    var name = `${user.salutation || ''} ${user.preferredName || user.firstName} ${user.lastName}`;

    return <div className="tfc-anniversary-user">
        <div className="tfc-anniversary-label">
            <span className="tfc-anniversary-date">{user.anniversary.format('D')}</span>
            <span className="tfc-anniversary-dayname">{user.anniversary.format('MMM')}</span>
        </div>
        <span className="tf-user-link">
            <a className="tf-miniprofile-user" data-userid={user.userId} href={`/content/${user.contentId}`}>{name}</a>
        </span>
    </div>;
};
```

  
**Step 5: Add styles**

Add the following to your Styles \(CSS\) tab:

```text
.tfc-anniversary .tfc-anniversary-list{
        padding-left: 10px;
}

.tfc-anniversary .tfc-anniversary-list .tfc-anniversary-item {
        list-style: none;
}

.tfc-anniversary .tfc-anniversary-list .tfc-anniversary-item  .tfc-anniversary-user {
        position: relative;
        margin: 6px 0;
}

.tfc-anniversary .tfc-anniversary-list .tfc-anniversary-user .tfc-anniversary-label {
        background: white;
        border: 1px solid #ccc;
        padding: 4px 0;
        display: inline-block;
        min-width: 31px;
        line-height: 1;
        vertical-align: middle;
}

.tfc-anniversary .tfc-anniversary-list .tfc-anniversary-user .tfc-anniversary-label .tfc-anniversary-date {
        display: block;
        letter-spacing: 1px;
        padding-bottom: 2px;
        text-align: center;
}
.tfc-anniversary .tfc-anniversary-list .tfc-anniversary-user .tfc-anniversary-label .tfc-anniversary-dayname {
        display: block;
        text-transform: uppercase;
        font-size: 9px;
        font-weight: 600;
        letter-spacing: 1px;
        text-align: center;
}

.tfc-anniversary .tfc-anniversary-list .tfc-anniversary-user .tf-user-link {
        display: inline-block;
        margin-left: 10px;
}
```

Once you have added all the necessary code in the editor, click the **Save** button. If you have saved your work along the way, you may be prompted to '**Update Card**'. Navigate back to the **Manage Cards** page, and slide the button to activate.  
  
Add your card to the page you wish it to appear on by clicking **Manage Cards** in the sidebar and then **Update Template.** Add your custom 'Work Anniversary' card. Save and view, and you will get back the users with work anniversaries in the current month.

![](../../.gitbook/assets/4%20%2820%29.png)

  
  


