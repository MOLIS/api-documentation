`/images`

Since this endpoint requires an upload, it behaves a little different. 

By definition the endpoint expects a pair of a form field ```imagen``` (the image file) and ```imagen-data``` (image meta data) where the meta data part is optional. Check the example below.

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
The endpoint expects an array of objects with the following fields:

<table>
  <tr>
    <td>Name</td>
    <td>Description</td>
    <td>Type</td>
    <td>Example / possible value</td>
  </tr>
  <tr>
    <td>imagen</td>
    <td><strong>required</strong> Image file</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>imagen-data</td>
    <td><strong>optional</strong> JSON string with image meta data</td>
    <td></td>
    <td><pre>{
  "tags":[
    {
      "id":"df36e64edec34937bb0cb4f533dd39e6"
    },
    {
      "id":"af93d2a6961a433ca35010c356a3d076"
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

{"tags":[{"id":"2d09ac22ec854c50b32450471e53d444"}]}
------WebKitFormBoundaryjI2vJePM8557uLDA
Content-Disposition: form-data; name="image-1"; filename="img1.jpg"
Content-Type: image/jpeg


------WebKitFormBoundaryjI2vJePM8557uLDA--
```

#### Response example

```
[
  {
    "id":"bb8ce3f6c0844ecb939627c30f0a9160",
    "files":{
      "large":"/somefolder/myFile_large.jpg",
      "medium":"/somefolder/myFile_medium.jpg",
      "small":"/somefolder/myFile_small.jpg",
    },
    "tags":[
      {
        "id":"2d09ac22ec854c50b32450471e53d444",
        "category":"some_category",
        "label":"some_label"
      }
    ]
  }
]
```

#### Errors (endpoint specific)

Priority is always to process the image upload since this is expensive. If something is wrong with the meta data, the uploaded image will still be processed. Also when one image of a batch upload is invalid, the others will be processed as expected.

**Error when one of two images is invalid**

```
[
  {
    "id":"bb8ce3f6c0844ecb939627c30f0a9160",
    "files":{
      "large":"/somefolder/myFile_large.jpg",
      "medium":"/somefolder/myFile_medium.jpg",
      "small":"/somefolder/myFile_small.jpg",
    },
    "tags":[]
  },
  {
    "error":"file_error",
  }
]
```

**Error when one of two images already exists**

For already uploaded images the id will be returned. Tags will **not** be updated.

```
[
  {
    "id":"bb8ce3f6c0844ecb939627c30f0a9160",
    "files":{
      "large":"/somefolder/myFile_large.jpg",
      "medium":"/somefolder/myFile_medium.jpg",
      "small":"/somefolder/myFile_small.jpg",
    },
    "tags":[]
  },
  {
    "id":"badfb1e4b1d6431b852d9c4b31ac1988", // image was previously uploaded
    "error":"image_already_exists"
  }
]
```

**Error when tag id does not exists**

```
[
  {
    "id":"bb8ce3f6c0844ecb939627c30f0a9160",
    "files":{
      "large":"/somefolder/myFile_large.jpg",
      "medium":"/somefolder/myFile_medium.jpg",
      "small":"/somefolder/myFile_small.jpg",
    },
    "tags":[
      {
        "id":"2693493ba3b3438e946460aa41e64db7", // not existing
        "error":"tag_error"
      }
    ]
  }
]
```