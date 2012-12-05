`http://api.molis.io/v1/tags/:id`

Returns a [tag obj](tag-object.md) with :id. The tag needs to belong to the authenticated user.

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
</table>

#### Response fields
<table>
  <tr>
    <td>tag</td>
    <td>A <a href="tag-object.md">tag object</a></td>
  </tr>
</table>

#### Examples
todo