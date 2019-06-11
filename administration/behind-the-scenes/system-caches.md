# System Caches

### System caches

The System caches are used to increase performance in ThoughtFarmer. You will very rarely need to use the functions on the **System caches** page. This page is typically only used when trying to troubleshoot support issues.  
  
**If you feel that you need to use the System caches screen we suggest that you contact** [**support@thoughtfarmer.com**](mailto:support@thoughtfarmer.com) **to help you understand the impact of any changes made and also to explain the function of each section in more detail.**  
  
The following is a brief overview of each of the functions.

### Refresh tree paths

The tree path is the location within the ThoughtFarmer hierachy where a specific piece of content can be found. The tree path is a calculated value. The values for the entire ThoughtFarmer site can be recalculated by clicking **Refresh tree paths**.

### Empty thumbnail image cache

When images stored within ThoughtFarmer are viewed at different sizes / dimensions the resized image is cached so that it does not need to be created every time it is requested. Clicking **Empty thumbnail image cache** will delete all of the stored resized images and they will be regenerated the next time they are requested.

### Object caching

This is a data cache that stores repeatedly used data from ThoughtFarmer in the web server's memory. This reduces the number of round trip calls to the database. Clicking **Flush cached data** will delete all of the data currently stored in the web server's memory and force the data to be retrieved from the database on the next request.

