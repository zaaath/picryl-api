# Collection Resources

    GET collections/:id/photos

## Description
Returns a listing of twenty (up to one hundred) collection photos.
***

## Parameters

- **page** — Return a specific page. Page numbering is 1-based.
- **rpp** — The number of results to return. Can not be over 100, default 20.
- **fields** - Comma separated list of fields. Allows restricting which fields are returned. If no fields are selected, all fields are returned.	


***

## Return format
An array with the following keys and values:

- **current_page** — Number of the page that is returned.
- **total_pages** — Total number of pages matching specified criteria.
- **total_items** — Total number of items matching specified criteria.
- **items** — An array of Photo objects.

***

## Errors

None
***

## Example
**Request**

    http://api.getarchive.net/v2/collection/79c1a9572a1918d2f239f446ed11f01e/photos

**Return** __shortened for example purpose__
``` json
{
  "current_page": 1,
  "total_pages": 2,
  "total_items": 25,
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
            "url": "http://d1qb4gn8ltk7f1.cloudfront.net/100/ca0632.photos.016181p.jpg"
        },
        {
            "size": 200,
            "url": "http://d1qb4gn8ltk7f1.cloudfront.net/200/ca0632.photos.016181p.jpg"
        },
        {
            "size": 640,
            "url": "http://d1qb4gn8ltk7f1.cloudfront.net/640/ca0632.photos.016181p.jpg"
        },
        {
            "size": 1024,
            "url": "http://d3mld3sq8wfq8f.cloudfront.net/1024/ca0632.photos.016181p.jpg"
        }
      ]
    }
  ]
}
```
