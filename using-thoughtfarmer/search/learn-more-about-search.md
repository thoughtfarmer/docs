# Learn more about search

### Search terms are individual words or phrases

There are two types of search terms: 1\) single terms and 2\) phrases.

A "single term" is an individual word such as "profile" or "photo." If you type in several terms \(words\) in your search query, search results will include pages \(or files or comments\) where one or both words can be found somewhere in the page. But the terms won't necessarily be next to each other or even in the same sentence or paragraph.  
  
A simple search includes one or more "single terms".  
  
**Example search**: profile instructions

### Use quotations \(" "\) to create an exact phrase 

A "phrase" is a group of several terms \(words\) surrounded by double quotes such as "profile photo". When you search for a phrase, only content that includes that exact phrase will show up in search results.  
  
For **example**, a search for "profile photo": 

* **Will include** a result that has this text: "_... use these instructions to select a great **profile photo**..._"
* **Will NOT include** a result that has this text: "_...use these instructions to update your **profile** with a **photo**..._"

### Terms use wildcard search and stemming

You can add \* to a search query to signify a wildcard search. \* in a search term represents that one or more characters can be present in that part of the search term. The \* can be put at the front, in the middle, or at the end of the search term.  
  
For **example**, perhaps you are searching for a person's name, but are not quite sure how to spell it. A search for **mi\*el**:

* **Will include** a result for Kerry Michel \(the \* in this case represents the "ch" in the name\).

Any term that you enter will automatically look for variations that include that term.  
  
For **example**, a search for "admin"

* **Will include** results that contain "Admin", "administrator", "administration", etc...

​As of ThoughtFarmer 8.1, search also performs stemming. This means that search determines the root or stem of the words you are searching for and looks for all the different variations. Search supports multilingual stemming for English, Spanish, French, Italian, Dutch, Portuguese, Russian, Turkish and English. Stemming is not supported for Korean, Japanese and Chinese.  
  
For **example**, a search for "uploader"  
 

* Will search for the root word "upload" and so **will include** results that contain "upload", "uploaded", "uploading", etc...

### Multilingual searches

As of ThoughtFarmer 8.1, search automatically prioritizes search results based on your language preferences. For example, if your preferred language is French, ThoughtFarmer will prioritize matches on the French language version of the page.

### Query expression searches

This kind of searching gets a bit more technical, and allows you to use symbols in your search to represent search operators. This type of search needs to have parentheses around it eg. \(search term\) in order to signify the type of search being used.  
  
The following query operators are allowed:

* + signifies AND operation
* \|\| signifies OR operation
* - negates a single term
* " wraps a number of terms to signify a phrase for searching
* \* signifies a wildcard \(one or more characters\) - this operator has been set up to not require parentheses around it
* ? signifies a wildcard \(single character\)
* \( and \) signify precedence
* ~N after a word signifies edit distance \(fuzziness\)
* ~N after a phrase signifies slop amount

The default operator in these queries is AND, not OR.  
  
Examples:

* The search **\(profile -photo\)** would return results that **include profile**, but **do not include photo**.
* The search **\(-profile photo\)** would return results that do not include profile, but **do include photo**.
* The search **\(document\* -video\)** would return results that **include documentary or documentation**, but **do not include video**.
* The search **\(document\* -documentary -documented -documentation\)** would return results that **include documents or documenting** but **do not include documentary, documented or documentation**.
* The search **\(profile + "tutorial video"\)** would return results that **do include profile and the exact phrase "tutorial video"**.

### Hot Intranet Tip!

Want to be a total Search+ pro?

1. Use CTRL + / \(or ⌘ + / for Mac users\) to bring up the search box.
2. Start typing your search term and then pause briefly to let the Search suggestions appear in the dropdown.
3. Use your arrow keys to navigate the Search suggestions and then hit Enter to go to your desired page.

Fast!

