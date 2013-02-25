## MOLIS API Documentation

#### Introduction

While the `/images` endpoint works mostly es expected (except maybe POST multipart/form-data) the `/tags` endpoint is more important then you might think. 

We use tags as universal weapon for adding meta data to images. Notice the `category` field in the [object documentation](tags-object.md). While it **can** be "freetext" (typical tags behavior) it can also have other purposes. If you're missing a category, [please leave an issue](https://github.com/MOLIS/api-documentation/issues).

#### Authentication

[More here](authentication.md)

#### Endpoints

<table>
  <tr>
    <td>Endpoint</td>
    <td>Method</td>
    <td>Description</td>
    <td>Full documentation</td>
  </tr>
  <tr>
    <td><code>/hello</code></td>
    <td><code>GET</code></td>
    <td>Returns user name and api version</td>
    <td><a href="get-hello.md">Read more</a></td>
  </tr>
  <tr>
    <td><code>/images</code></td>
    <td><code>GET</code></td>
    <td>Returns array of images</td>
    <td><a href="get-images.md">Read more</a></td>
  </tr>
  <tr>
    <td></td>
    <td><code>POST (multipart/form-data)</code></td>
    <td>Upload new images</td>
    <td><a href="post-images.md">Read more</a></td>
  </tr>
  <tr>
    <td></td>
    <td><code>PUT</code></td>
    <td>Batch update images</td>
    <td><a href="put-images.md">Read more</a></td>
  </tr>
  <tr>
    <td><code>/images/:id</code></td>
    <td><code>GET</code></td>
    <td>Get image object of image with :id</td>
    <td><a href="get-images-id.md">Read more</a></td>
  </tr>
  <tr>
    <td></td>
    <td><code>PUT</code></td>
    <td>Update image object of image with :id</td>
    <td><a href="put-images-id.md">Read more</a></td>
  </tr>
  <tr>
    <td><code>/tags</code></td>
    <td><code>GET</code></td>
    <td>Returns array of tags</td>
    <td><a href="get-tags.md">Read more</a></td>
  </tr>
  <tr>
    <td></td>
    <td><code>POST</code></td>
    <td>Creates new tags</td>
    <td><a href="post-tags.md">Read more</a></td>
  </tr>
  <tr>
    <td></td>
    <td><code>PUT</code></td>
    <td>Batch update tags</td>
    <td><a href="put-tags.md">Read more</a></td>
  </tr>
  <tr>
    <td><code>/tags/:id</code></td>
    <td><code>GET</code></td>
    <td>Get tag object of tag with :id</td>
    <td><a href="get-tags-id.md">Read more</a></td>
  </tr>
  <tr>
    <td></td>
    <td><code>PUT</code></td>
    <td>Update tag object of tag with :id</td>
    <td><a href="put-tags-id.md">Read more</a></td>
  </tr>
</table>

#### Response Objects

<table>
  <tr>
    <td>Image</td>
    <td><a href="image-object.md">Read more</a></td>
  </tr>
  <tr>
    <td>Tag</td>
    <td><a href="tag-object.md">Read more</a></td>
  </tr>
</table>