`/tags/:id`

Update tag with :id.

<strong>Note:</strong> Currently only changing the ```images``` property is allowed.

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
The endpoint expects either a tag object that looks like this:

<table>
  <tr>
    <td>Name</td>
    <td>Description</td>
    <td>Type</td>
    <td>Example / possible value</td>
  </tr>
  <tr>
    <td>images</td>
    <td><strong>required</strong> Array with objects wirth image id's</td>
    <td><code>Array</code></td>
    <td><pre>[
  {
    "id":"imageId1"
  }, 
  {
    "id":"imageId2"
  }, 
  {
    "id":"imageId3"
  }
]</pre></td>
  </tr>
</table>


#### Response fields
Updated <a href="tag-object.md">tag object</a>.

#### Examples
todo