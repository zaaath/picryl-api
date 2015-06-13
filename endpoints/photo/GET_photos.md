# Photo Resources

    GET photos

## Description
Returns a listing of twenty (up to one hundred) photos matching some criteria.
***

## Parameters

- **tags** — String name of the **[tag]()** to return photos for. **Note:** Separate multiple values with a comma.
- **date_from** 
- **date_to**

- **page** — Return a specific page in the photo stream. Page numbering is 1-based.
- **rpp** — The number of results to return. Can not be over 100, default 20.

- **image_size** — The photo size(s) to be returned. See the documentation on **[photo sizes][]**. ???
- **fields** ???
 
- **sort** — Sort photos in the specified order. ???
    ###### Recognized values:
    - 'times_viewed' — Sort by view count
    - 'created_at' — Sort by the original date of the image extracted from metadata (might not be available for all images)

- **sort_direction** — Control the order of the sorting.  You can provide a **sort_direction** without providing a **sort**, in which case the default sort for the requested feature will be adjusted.
    ###### Recognized values:
    - 'asc' — Sort in ascending order (lowest or least-recent first)
    - 'desc' — Sort in descending order (highest or most-recent first).  This is the default.


***

## Return format
An array with the following keys and values:

- **current_page** — Number of the page that is returned.
- **total_pages** — Total number of pages matching specified criteria.
- **total_items** — Total number of items matching specified criteria.
- **items** — An array of Photo objects. If fields is specified ...???

***

## Errors

None
***

## Example
???
