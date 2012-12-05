`http://api.molis.io/v1/tags`

Batch update tags.

<strong>Note:</strong> Currently only changing the ```images`` property is allowed.

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
The endpoint expects an array of tag objects. The expected tag object looks like this:

<table>
  <tr>
    <td>Name</td>
    <td>Description</td>
    <td>Type</td>
    <td>Example / possible value</td>
  </tr>
  <tr>
    <td>id</td>
    <td><strong>required</strong> Id of the tag to update</td>
    <td><code>String</code></td>
    <td><code>"ABC123"</code></td>
  </tr>
  <tr>
    <td>images</td>
    <td><strong>required</strong> Image id's</td>
    <td><code>Array</code></td>
    <td><pre>[
  {
    "id":"8f0ef7602cbd11e281c10800200c9a66"
  }, 
  {
    "id":"94a3f3b02cbd11e281c10800200c9a66"
  }, 
  {
    "id":"99dffa902cbd11e281c10800200c9a66"
  }
]</pre></td>
  </tr>
</table>


#### Response fields
Array of <a href="tag-object.md">tag object's</a>.

#### Examples
todo
