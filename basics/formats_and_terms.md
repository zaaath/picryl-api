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

# TODO what if size not available for image?

Picryl has a number of preset image sizes.  Most API requests that return image URLs can be instructed to return the URLs for one or more specific sizes.  To retrieve the URL for a specific image size, include that size's ID in the query string of the request, using the `image_size` parameter:

```
GET /v2/photos?image_size=3
```

If you want to request multiple sizes, you can pass an comma separated value for `image_size` as well:
```
GET /v1/photos?image_size=2,600
```

These are the standard cropped sizes:
<table id="image_sizes">
  <tr>
    <th>ID</th>
    <th>Dimensions</th>
  </tr>
  <tr><td>1</td><td>70px x 70px</td></tr>
  <tr><td>2</td><td>140px x 140px</td></tr>
  <tr><td>3</td><td>280px x 280px</td></tr>
  <tr><td>100</td><td>100px x 100px</td></tr>
  <tr><td>200</td><td>200px x 200px</td></tr>
  <tr><td>440</td><td>440px x 440px</td></tr>
  <tr><td>600</td><td>600px x 600px</td></tr>
</table>

These are the standard uncropped sizes:
<table id="image_sizes">
  <tr>
    <th>ID</th>
    <th>Dimensions</th>
  </tr>
  <tr><td>4</td><td>900px on the longest edge</td></tr>
  <tr><td>5</td><td>1170px on the longest edge</td></tr>
  <tr><td>20</td><td>300px high</td></tr>
  <tr><td>21</td><td>600px high</td></tr>
  <tr><td>30</td><td>256px on the longest edge</td></tr>
  <tr><td>1080</td><td>1080px on the longest edge</td></tr>
  <tr><td>1600</td><td>1600px on the longest edge</td></tr>
  <tr><td>2048</td><td>2048px on the longest edge</td></tr>
</table>
***
