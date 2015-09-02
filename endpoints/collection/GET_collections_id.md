# Collection Resources

    GET collections/:id

## Description
Returns detailed information of a single collection.

***

## Parameters

- **fields** - Comma separated list of fields. Allows restricting which fields are returned. If no fields are selected, all fields are returned.
- **include_photos** - The number of collection photos to include. Can not be over 20.

***

## Return format
Collection object.

***

## Errors
All known errors cause the resource to return HTTP error code header together with a JSON array containing at least 'status' and 'error' keys describing the source of error.

- **404 Not Found** — Collection with the specified ID does not exist.


***

## Example
**Request**

    http://api.getarchive.net/v2/collection/79c1a9572a1918d2f239f446ed11f01e?include_photos=5

**Return** __shortened for example purpose__
``` json
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
```
