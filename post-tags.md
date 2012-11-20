`/tags`

* HTTP method: POST
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
    <td>category</td>
    <td><strong>required</strong> Category of the tag</td>
    <td><code>String</code></td>
    <td><code>"event"</code>,<code>"location"</code>, <code>"person"</code> or <code>"freetext"</code></td>
  </tr>
  <tr>
    <td>label</td>
    <td><strong>required</strong> Name of the tag</td>
    <td><code>String</code></td>
    <td><code>"Emily"</code>, <code>"Mom's and Dad's House"</code>, <code>"Asia vacation"</code></td>
  </tr>
  <tr>
    <td>images</td>
    <td><strong>optional</strong> Array with obj's with image id's</td>
    <td><code>Array</code></td>
    <td><pre>[
  {
    "id":"6833c3002cbd11e281c10800200c9a66"
  }, 
  {
    "id":"7a19abc02cbd11e281c10800200c9a66"
  }, 
  {
    "id":"8072bb602cbd11e281c10800200c9a66"
  }
]</pre></td>
  </tr>
</table>

#### Response fields
Array of created <a href="tag-object.md">tag object</a>.

#### Example
todo