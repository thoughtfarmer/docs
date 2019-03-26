# Photo gallery setting

### Choose default gallery sort order

Photos on gallery pages can be sorted by date uploaded \(from newest to oldest\), by popularity, and by the curated order that a page editor has chosen.  
  
Administrators can set the default sort order for galleries using a config setting.  
 

1. Go to the **Administration panel**: **Advanced options** section &gt; **Configuration settings** page.
2. Type **photo** in the **Search config settings** field to narrow the config settings results.
3. Find the config setting photogallery.defaultSortOrder.
4. Click in the **Value** column beside the config setting, and type the desired value:
   1. 0 = Default sort order for all users is Curated
   2. 1 = Default sort order for all users is Popular
   3. 2 = Default sort order for all users is Date uploaded \(newest to oldest\)
   4. -1 = Default sort order is whatever the user last set it to.
5. Click **Save**.

### Enable compact view for large galleries

A compact view of photo galleries is available for photo galleries that contain a large number of images. In compact view, the image thumbnails are smaller, reducing the amount that has to load on the page. Intranet administrators can determine the maximum number of photos a gallery can contain before displaying in compact view. The default maximum number of images is 40.

![](../../../.gitbook/assets/3%20%2864%29.jpg)

**Gallery in compact view**

![](../../../.gitbook/assets/4%20%2819%29.jpg)



1. Go to the **Administration panel**: **Advanced options** section &gt; **Configuration settings** page.
2. Type **photo** in the **Search config settings** field to narrow the config settings results.
3. Find the config setting photogallery.compactViewCount.
4. Click in the **Value** column beside the config setting and enter a value for the maximum number of photos in a gallery before it displays in compact view.
5. Click **Save**.

### Enable "load more" action for large galleries

For galleries with many images, administrators can set the maximum number of rows of images that will display without the user clicking the Load more action at the bottom of the images. The default number of rows is 5.  
 

1. Go to the **Administration panel**: **Advanced options** section &gt; **Configuration settings** page.
2. Type photo in the **Search config settings** field to narrow the config settings results.
3. Find the config setting photogallery.loadMoreRowCount.
4. Click in the **Value** column beside the config setting and enter the maximum number of rows that will display before a user clicks "Load more" at the bottom of the gallery.
5. Click **Save**.

