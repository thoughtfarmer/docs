# Search index

### Search index

ThoughtFarmer 8.1 and above uses the ElasticSearch search engine for high-performance, full-featured indexing of pages and supported attachment file types. Read this page for information on configuring the search index, or see [Troubleshooting the search index](troubleshooting-the-search-index.md).

### Re-Indexing ThoughtFarmer <a id="section2"></a>

At any time an administrator can re-index the entire site. This action will go through all of the content in the site and rebuild the index from scratch. Depending on the number of content items and server performance, this can take some time.  
  
Re-indexing the site should not need to be performed regularly. It is only a remedy for when there is a problem with search on the site. Please see [Troubleshooting the search index ](troubleshooting-the-search-index.md)for guidance on when to re-index.

### Supported attachments and IFilters <a id="section3"></a>

The content for any attachments uploaded to ThoughtFarmer can also be added to the index. This allows for search to return results for queries that match content inside the actual attachment. The ability to support indexing of a particular file type is dependent on the IFilters that are installed on the web server. The default ThoughtFarmer checklist requires that the following IFilters be installed:  
  
**Microsoft 2.0 Filter Pack**: Allows for indexing of all MS Office file types.  
  
Please see either the [Windows Server 2008](https://community.thoughtfarmer.com/content/10404), or [Windows Server 2012](https://community.thoughtfarmer.com/content/10386) pages for links to the proper versions of the above filter pack.  
  
Additional file types can be indexed if there exists a Windows compatible IFilter for them. To add an IFilter for a new file type and make it available for ThoughtFarmer indexing you will need to configure both the server and ThoughtFarmer accordingly.

#### Adding a new attachment type for indexing

1. Install the IFilter on the ThoughtFarmer web server.
2. On the server go to **Start** &gt; **Administrative Tools** &gt; **Services**. Look for the ThoughtFarmer Service and restart it.
3. Go to the ThoughtFarmer **Administration Panel**: **Advanced options** section &gt; **Configuration settings**page.
4. Search for the config setting files.extractedText.extensions and click in the **Value** column to add the appropriate extension\(s\) to the list. Click **Save**.
5. Go to the ThoughtFarmer **Administration Panel**: **Search** section &gt; **Search settings** page, **Index** tab. Click **Update extracted text**.
6. Wait for that to finish and then click **Rebuild index** on the same page.

The update may take some time to complete depending the amount of content on your intranet and your server specifications.

