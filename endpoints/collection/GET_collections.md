# Collection Resources

    GET collections

## Description
Returns a listing of twenty (up to one hundred) collections.
***

## Parameters

- **page** — Return a specific page. Page numbering is 1-based.
- **rpp** — The number of results to return. Can not be over 100, default 20.
- **fields** - Comma separated list of fields. Allows restricting which fields are returned. If no fields are selected, all fields are returned.	
- **include_photos** - The number of collection photos to include. Can not be over 20.


***

## Return format
An array with the following keys and values:

- **current_page** — Number of the page that is returned.
- **total_pages** — Total number of pages matching specified criteria.
- **total_items** — Total number of items matching specified criteria.
- **items** — An array of Collection objects.

***

## Errors

None
***

## Example
**Request**

    http://api.getarchive.net/v2/collections

TODO example response

**Return** __shortened for example purpose__
``` json
{
  "current_page": 1,
  "total_pages": 2,
  "total_items": 21,
  "items": [
      {
      "id": "79c1a9572a1918d2f239f446ed11f01e",
      "name": "Frank Meadow Sutcliffe (England, 1853-1941)",
      "total_photos": 24,
      "photos": [
        {
          "id": "3368ad59420edba4f60195afd4203a95",
          "name": "Sunshine & Shower"
        }
      ]
    }
  ]
}
```
