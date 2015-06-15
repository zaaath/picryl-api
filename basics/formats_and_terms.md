# Formats and Terms

## Photo object

Photo object includes the following data:

- **id** — ID of the photo, string
- **name** — Title of the photo, string
- **min_created_date** - Timestamp indicating the bottom bound date of photo creation, timestamp
- **max_created_date** - Timestamp indicating the top bound date of photo creation, timestamp
- **tags** - List of tags representing a photo, array
- **location** — A human-readable name of the location where the photo was taken, string
- **latitude** — Latitude of the location where the photo was taken, decimal
- **longitude** — Longitude of the location where the photo was taken, decimal
- **creators** - List of people involved in the creation of photo, array
- **source_name** - Place of original publication of photo, string
- **source_url** - Original publication URL, string
- **images** - Array with images URL and sizes

***


## Image Sizes

You'll find the URLs to the image(s) for a photo in the `images` field in the returned JSON for a photo.

<!--**Important** - You must not alter the URLs returned by the API in any way. Instead, please use the `image_size` parameter to request the sizes your application needs.-->

Picryl has a number of preset image sizes.  

These are the standard cropped sizes:
- 100px x 100px
- 200px x 200px

These are the standard uncropped sizes:
- 1024px on the longest edge
- 640px on the longest edge
 

***
