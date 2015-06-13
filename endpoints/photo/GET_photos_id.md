# Photo Resources

    GET photos/:id

## Description
Returns detailed information of a single photo.

***

## Parameters

- **image_size** — The photo size(s) to be returned. See the documentation on **[photo sizes](https://github.com/picryl/picryl-api/blob/master/basics/formats_and_terms.md#image-sizes)**.
- **fields** - Comma separated list of fields. Allows restricting which fields are returned. If no fields are selected, all fields are returned.

***

## Return format
Photo object.

***

## Errors
All known errors cause the resource to return HTTP error code header together with a JSON array containing at least 'status' and 'error' keys describing the source of error.

- **404 Not Found** — Photo with the specified ID does not exist.


***

## Example
**Request**

    http://46.101.149.102/api/v2/photos/4910421

**Return** __shortened for example purpose__
``` json
{
  "id": "4910421",
  "name": "Franklin before the lord's council, Whitehall Chapel, London, 1774",
  "min_created_date": "1774-01-01",
  "max_created_date": "1774-01-01",
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
  "images": []
}
```
