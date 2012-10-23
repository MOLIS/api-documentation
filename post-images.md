`/images`

Since this endpoint requires an upload, it behaves a little different. 

By definition the endpoint expects a pair of a form field ```image-n``` (the image file) and ```image-n-data``` (image meta data) where the meta data part is optional. Check the example below.

* HTTP method: POST (multipart/form-data)
* Token required: Yes

#### Parameters
All parameters are optional, unless otherwise indicated.
<table>
  <tr>
    <td>Name</td>
    <td>Description</td>
    <td>Example</td>
  </tr>
  <tr>
    <td>token</td>
    <td><strong>required</strong> OAuth token</td>
    <td><code>?token=ABC123</td>
  </tr>
</table>

#### Request fields
The endpoint expects either a single image object or an array of image objects. The expected image object looks like this:

<table>
  <tr>
    <td>Name</td>
    <td>Description</td>
    <td>Type</td>
    <td>Example / possible value</td>
  </tr>
  <tr>
    <td>image-n</td>
    <td><strong>required</strong> Image file</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>image-n-data</td>
    <td><strong>optional</strong> JSON string with image meta data</td>
    <td></td>
    <td><pre>{
  "tags":[
    {
      "id:""ABC123"
    },
    {
      "id":"DEF456"
    }
  ]
}</pre></td>
  </tr>
</table>


#### Response fields
An array of created <a href="image-object.md">image object</a>'s.

#### Request example
```
------WebKitFormBoundaryjI2vJePM8557uLDA
Content-Disposition: form-data; name="image-1-data"

{"tags":[{"id":"ABC123"}]}
------WebKitFormBoundaryjI2vJePM8557uLDA
Content-Disposition: form-data; name="image-1"; filename="img1.jpg"
Content-Type: image/jpeg


------WebKitFormBoundaryjI2vJePM8557uLDA--
``
