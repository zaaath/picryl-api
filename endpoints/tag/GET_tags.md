# Photo Resources

    GET tags

## Description
Returns a listing of twenty (up to one hundred) tags matching some criteria.
***


## Parameters
- **starts_with** — String fragment to search for.
- **page** — Return a specific page in the photo stream. Page numbering is 1-based.
- **rpp** — The number of results to return. Can not be over 100, default 20.

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

    http://46.101.149.102/api/v2/tags?starts_with=lond

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
        "http://lcweb2.loc.gov/service/pnp/habshaer/va/va0900/va0974/photos/165168p_150px.jpg",
        "http://lcweb2.loc.gov/service/pnp/habshaer/va/va0900/va0974/photos/165169p_150px.jpg",
        "http://lcweb2.loc.gov/service/pnp/habshaer/va/va0900/va0974/photos/165170p_150px.jpg",
        "http://lcweb2.loc.gov/service/pnp/habshaer/va/va0900/va0974/sheet/00001_150px.jpg",
        "http://lcweb2.loc.gov/service/pnp/habshaer/va/va0900/va0974/sheet/00002_150px.jpg"
      ],
      "count": 5157
    }
  ]
}
```
