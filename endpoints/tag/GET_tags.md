# Photo Resources

    GET tags

## Description
Returns a listing of twenty (up to one hundred) tags matching some criteria.
***


## Parameters

- **starts_with** — String fragment to search for.
- **page** — Return a specific page. Page numbering is 1-based.
- **rpp** — The number of results to return. Can not be over 100, default 20.

- **sort** — Sort tags in the specified order.
    ###### Recognized values:
    - 'frequency' — The most frequent tags first. This is the default.
    - 'trending' — trending tags first


***

## Return format
An array with the following keys and values:

- **current_page** — Number of the page that is returned.
- **total_pages** — Total number of pages matching specified criteria.
- **total_items** — Total number of items matching specified criteria.
- **items** — An array of Tag objects.

***

## Errors

None
***

## Example
**Request**

    http://api.getarchive.net/v2/tags?starts_with=lond

**Return** __shortened for example purpose__
``` json
{
  "current_page": 1,
  "total_pages": 250,
  "total_items": 5000,
  "items": [
    {
      "id": "london",
      "thumbs": [
        "http://d1qb4gn8ltk7f1.cloudfront.net/100/ca0625.photos.016843p.jpg",
        "http://d1qb4gn8ltk7f1.cloudfront.net/100/ca0625.photos.016856p.jpg",
        "http://d1qb4gn8ltk7f1.cloudfront.net/100/ca0625.photos.165170p.jpg",
        "http://d1qb4gn8ltk7f1.cloudfront.net/100/ca0625.photos.016878p.jpg",
        "http://d1qb4gn8ltk7f1.cloudfront.net/100/ca0625.photos.165179p.jpg"
      ],
      "count": 5157
    }
  ]
}
```
