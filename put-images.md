`/images`

Batch update images.

* HTTP method: PUT
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
    <td>id</td>
    <td><strong>required</strong> Id of the image to update</td>
    <td><code>String</code></td>
    <td><code>"ABC123"</code></td>
  </tr>
  <tr>
    <td>tags</td>
    <td><strong>required</strong> Updated array of object's with tag id</td>
    <td><code>Array</code></td>
    <td><pre>[
  {
    "id:""ABC123"
  },
  {
    "id":"DEF456"
  }
]</pre></td>
  </tr>
</table>


#### Response fields
An array of created <a href="image-object.md">image objects</a>.

#### Examples
todo
