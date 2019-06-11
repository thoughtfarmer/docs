# Learn more about ThoughtFarmer search+



As of version 8.5, ThoughtFarmer uses a brand new search engine, Search+. It's a modern search engine with many new features, including better relevance ranking, faster results, multilingual stemming support and many other frequently requested features.

#### **Architecture**

ThoughtFarmer's Search+ engine powers the search results, faceted search and the activity feed, people directory and group directory. It runs as a stand-alone service alongside the ThoughtFarmer Service.  
  
The ThoughtFarmer Search+ engine uses the ElasticSearch library, one of the leading full-text search engines. We've modified and configured it to work best for intranet searching.   
  
Every time you add or edit content or attachments in ThoughtFarmer, the text content is extracted and indexed inside the search service. You can rebuild the index via the admin panel. While the search index is being rebuilt, search results on your intranet will be incomplete. Search index rebuilds are much faster in TF 8.1+ - on our Cloud environment, rebuilding a 100,000 item database takes around 10 mins vs 60 minutes in TF 8.0.  
 

#### **Searching**

When you perform a search in ThoughtFarmer, a number of processes happen to ensure that you get the best possible search results. These include:  
 

* **Stemming.** ThoughtFarmer Search+ determines the root of the words you are searching for and looks for all the different variations. ThoughtFarmer supports multilingual stemming for English, Spanish, French, Italian, Dutch, Portuguese, Russian, Turkish and English. Stemming is not supported for Korean, Japanese and Chinese.
  * For example, searching for _running club_ will also match _run club_.
* **Keyword vs Exact Phrase Searches.** ThoughtFarmer Search+ defaults to a keyword search that will look for content with as many of your keywords as possible. However, pages that do not have every keyword may also be returned. To search for specific terms or exact phrases, add quotes around your search terms.
  * For example, a search for _Q1 2015 Financial Results_ may return searches for other quarters.  Searching for _"Q1 2015 Financial Results"_ will only return content that contains this exact phrase.
* **Stop word filtering.** By default, many common words \(e.g. and, but, to, etc.\) are filtered from the search index. Searches for these terms will be ignored. If you wish to add or remove items to the stop word list, they can be managed from the ThoughtFarmer Administration panel.
* **Multilingual searches.** ThoughtFarmer Search+ automatically prioritizes search results based on your language preferences.
  * For example, if your preferred language is French, ThoughtFarmer will prioritize matches on the French language version of the page. 

#### Results

ThoughtFarmer's Search+ results are sorted by relevance to surface the best possible results at the top. ThoughtFarmer uses a relevance ranking algorithm that takes many different factors into account to create an overall relevance score. Administrators can view the score by switching to Admin Mode.  
  
The following factors influence the score. Note that the score calculation is not a matter of adding together all the individual rankings, it is based primarily on the maximum score for each of the search factors.  
 

* **Location of matching terms.** ThoughtFarmer Search+ searches across all the fields of your content \(e.g. title, body of page, comments\) and will boost the score depending on the location. 
  * For example, pages with keyword matches in the Title rank higher than pages with keyword matches in the body. Pages that have tags that match the search keywords will also be scored higher.
* **Page type.** Results that match certain page types are boosted. 
  * For example, section pages are boosted above other pages, while comments have a negative boost. This is because top level sections often have minimal content compared to other pages.
* **Frequency of terms.** Pages that use a search term multiple times will rank higher than pages that use it fewer times.
* **Number of matching keywords.** When using multiple search terms, page matches that include all of the terms will rank higher than pages that only have 2 or 3 of the terms.
* **Page Popularity.** Pages that have been recently viewed, liked and commented on in the last 3 months will rank higher.
* **Calendar event dates.** Matches on calendar events from the past will rank lower than events in the future. 
  * For example, results for a search of _staff picnic_ will match events in the future higher than those in the past.

#### Additional Search Features

ThoughtFarmer Search+ has a number of additional features to help intranet users find content fast.  
 

* **Did you mean?** If users search for a misspelled word, ThoughtFarmer attempts to correct the spelling. The algorithm learns based on the content of your intranet - so if the word is misspelled in your content, ThoughtFarmer will not attempt to correct the spelling.
* **Best Bets.** Certain pages are often searched for with synonyms. You could add these synonyms to the body of the content or tags, but you can also help your users find these pages with Best Bets. When a user enters a Best Bet keyword, the page will appear at the top of the search results. Best Bets can be configured from the ThoughtFarmer Administration panel.
* **Find as you type.** When searching from the main search box, ThoughtFarmer will automatically search the intranet when you briefly pause typing. Power user tip: Use Ctrl-/ \(⌘-/ for Mac users\) to bring up the search box, and use the arrow keys and enter to navigate to your desired page. Fast!
* **Search term reporting.** Administrators can track what terms users are searching for from the Administration screen. Use this information to track what users are looking for and identify ways to improve your content, tagging or Best Bets. To learn more, see [Search term reports.](untitled-8.md)

### Learn more:

* [Find people and content with Search+](./)
* [Customize Search+ Settings](untitled-10.md)
* [Use Best Bets](untitled-9.md)
* [More about Search \(advanced user documentation\)](../../using-thoughtfarmer/search/learn-more-about-search.md)

