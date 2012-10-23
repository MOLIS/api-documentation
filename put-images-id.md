`/images/:id`

Update image with :id.

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
The endpoint expects either a single image object that looks like this:

<table>
  <tr>
    <td>Name</td>
    <td>Description</td>
    <td>Type</td>
    <td>Example / possible value</td>
  </tr>
  <tr>
    <td>tags</td>
    <td><strong>required</strong> Array of object's with tag id's</td>
    <td><code>Array</code></td>
    <td><pre>[
  {
    "id":"ABC123"
  }, 
  {
    "id":"DEF456"
  }
]</pre></td>
  </tr>
</table>


#### Response fields
Updated <a href="image-object.md">image object</a>.

#### Examples
todo