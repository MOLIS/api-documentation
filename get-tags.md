`/tags`

Returns all [tag obj](tag-object.md)'s of the authenticated user.

* HTTP method: GET
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
  <tr>
    <td>include_images</td>
    <td>Will return <a href="image-object.md">image obj</a> that have this tag</td>
    <td><code>?include_images=true, default: false</code></td>
  </tr>
</table>

#### Response fields
<table>
  <tr>
    <td>tags</td>
    <td>An Array of <a href="tags-object.md">tag objects</a></td>
  </tr>
</table>

**Note:** Currently there is no pagination implemented. The endpoint will return **all** tags, no matter how many there are. [This will change soon](https://github.com/MOLIS/api-documentation/issues/1).

#### Examples
todo