### Tag obj

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
    <td>A unique of the image (or video or audio)</td>
    <td><code>String</code></td>
    <td><code>"85566c1a597042c7b6e95fe5f9760d79"</code></td>
  </tr>
  <tr>
    <td>category</td>
    <td>Category of the tag</td>
    <td><code>String</code></td>
    <td><code>"event"</code>,<code>"location"</code>, <code>"person"</code> or <code>"freetext"</code></td>
  </tr>
  <tr>
    <td>label</td>
    <td>Name of the tag</td>
    <td><code>String</code></td>
    <td><code>"Emily"</code>, <code>"Mom's and Dad's House"</code>, <code>"Asia vacation"</code></td>
  </tr>
  <tr>
    <td>images</td>
    <td><strong>optional</strong> Array of <a href="image-object.md">image objects</a> that are tagged with this tag. Is only included in the response if endpoint was called with parameter <code>include_images=true</code>. Note: Image object will have no <code>tags</code> property.</td>
    <td><code>Array</code></td>
    <td><pre>[
  <a href="image-object.md">image object</a>,
  <a href="image-object.md">image object</a>
]</pre></td>
  </tr>
</table>
