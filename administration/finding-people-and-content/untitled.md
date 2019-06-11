# Tussenvoegsel search

Dutch surnames may contain tussenvoegsels, or words such as "van" or "de", that are excluded when alphabetizing a list of Dutch names. Two configuration settings have been added to ThoughtFarmer to allow for these terms to be excluded when alphabetizing names.  
  
**Example:**  
Alphabetical order with tussenvoegsel search enabled:van Dyke  
Pennal  
de Vries  
van der Winkel  
 Alphabetical order with tussenvoegsel search disabled:de Vries  
Pennal  
van der Winkel  
van Dyke  
When tussenvoegsels support is turned on, searching for any tussenvoegsels on the people page will not return any results. Tussenvoegsels will also be excluded when filtering the people page by first letter of last name. eg. Peter de Vries will show under "V" not "D".

### Change the tussenvoegsel configuration settings

1. Go to the **Administration panel**: **Advanced options** section &gt; **Configuration settings** page.
2. Type **tussen** in the **Search config settings** box to refine the results.
3. Click in the **Value** column beside the appropriate setting and change to the desired value as described below.
4. Click **Save**.

After enabling or disabling the tussenvoegsel search, you **must rebuild the search index** for the change to take effect. To rebuild the search index, go to the **Administration panel**: **Search** section &gt; **Search index** page.

**localization.tussenvoegsels.enabled**

Set to **true** to exclude tussenvoegsels from last names in the search index.  
Set to **false** to include tussenvoegsels in last names in the search index.

**localization.tussenvoegsels**

This configuration setting has a comma-delimited list of tussenvoegsels that will be excluded when the setting localization.tussenvoegsels.enabled is set to true.

