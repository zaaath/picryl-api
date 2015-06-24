# Photo Resources

    GET photos

## Description
Returns a listing of twenty (up to one hundred) photos matching some criteria.
***

## Parameters

- **tags** — Comma separated list of the tag to return photos for.
- **created_date_from** - If specified, include only photos created on or after this date. Dates should be submitted in ISO 8601 format (i.e., YYYY-MM-DD).
- **created_date_to** - If specified, include only images created on or before this date. Dates should be submitted in ISO 8601 format (i.e., YYYY-MM-DD).
- **page** — Return a specific page. Page numbering is 1-based.
- **rpp** — The number of results to return. Can not be over 100, default 20.
- **fields** - Comma separated list of fields. Allows restricting which fields are returned. If no fields are selected, all fields are returned.	
- **recommend_tags** - If set to 1, returns an array of recommended tags for the query.
- **sort** — Sort photos in the specified order. 
    ###### Recognized values:
    - 'times_viewed' — Sort by view count
    - 'created_date' — Sort by created date

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
- **items** — An array of Photo objects.
- **recommended_tags** - An array of recommended tags.

***

## Errors

None
***

## Example
**Request**

    http://getarchive.net/api/v2/photos?tags=london&recommend_tags=1

**Return** __shortened for example purpose__
``` json
{
  "current_page": 1,
  "total_pages": 250,
  "total_items": 5000,
  "recommended_tags": ["winston сhurchill", "british museum", "world war ii"],
  "items": [
    {
      "id": "4910421",
      "name": "Franklin before the lord's council, Whitehall Chapel, London, 1774",
      "min_created_date": "1774-01-01T00:00:00.000Z",
      "max_created_date": "1775-01-01T00:00:00.000Z",
      "tags": [
        "franklin",
        "chapel",
        "whitehall chapel",
        "london"
      ],
      "location": "London",
      "latitude": 51.5123793,
      "longitude": -0.1244296,
      "creators": [
        {
            "role": "engraver",
            "title": "Whitechurch, Robert, 1814-approximately 1880"
        }
      ],
      "source_name": "Library of Congress",
      "source_url": "http://www.loc.gov/pictures/item/00650385/",
      "images": [
        {
            "size": 100,
            "url": "http://getarchive.net/media/images/100/ca0632.photos.016181p.jpg"
        },
        {
            "size": 200,
            "url": "http://getarchive.net/media/images/200/ca0632.photos.016181p.jpg"
        },
        {
            "size": 640,
            "url": "http://getarchive.net/media/images/640/ca0632.photos.016181p.jpg"
        },
        {
            "size": 1024,
            "url": "http://getarchive.net/media/images/1024/ca0632.photos.016181p.jpg"
        }
      ]
    }
  ]
}
```
