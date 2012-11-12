### Image obj

#### Fields 
<table>
  <tr>
    <td>Name</td>
    <td>Description</td>
    <td>Type</td>
    <td>Example / possible value</td>
  </tr>
  <tr>
    <td>id</td>
    <td>A unique id of the image</td>
    <td><code>String</code></td>
    <td><code>"75656f021f8f455dbd926f1a513bd13a"</code></td>
  </tr>
  <tr>
    <td>files</td>
    <td>Object with paths to the image files. <a href="image-sizes.md">Read more about the image sizes</a></td>
    <td><code>Object</code></td>
    <td><pre>{
    original:"1bac96002cbe11e281c10800200c9a66.jpg",
    large:"1bac96002cbe11e281c10800200c9a66-large.jpg",
    medium:"1bac96002cbe11e281c10800200c9a66-medium.jpg",
    small:"1bac96002cbe11e281c10800200c9a66-small.jpg",
    thumb:"1bac96002cbe11e281c10800200c9a66-thumb.jpg"
}</pre></td>
  </tr>
  <tr>
    <td>tags</td>
    <td><strong>optional</strong> Array of <a href="tag-object.md">tag objects</a> of the image. Is only included in the response if endpoint was called with parameter <code>include_tags=true</code>. Note: Tag object will have no <code>images</code> property.</td>
    <td><code>Array</code></td>
    <td><pre>[
  <a href="tag-object.md">tag object</a>,
  <a href="tag-object.md">tag object</a>
]</pre></td>
  </tr>
</table>
