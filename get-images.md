`/images`

Returns all [image obj](image-object.md)'s of the authenticated user.

* HTTP method: GET
* Token required: Yes

####Parameters
All parameters are optional, unless otherwise indicated.
<table>
  <tr>
    <td>Name</td>
    <td>Description</td>
    <td>Default</td>
    <td>Example</td>
  </tr>
  <tr>
    <td>token</td>
    <td><strong>required</strong> OAuth token</td>
    <td></td>
    <td><code>?token=ABC123</td>
  </tr>
  <tr>
    <td>include_tags</td>
    <td>If true, every image object will come with a complete tag object array</td>
    <td><code>false</code></td>
    <td><code>?inlude_tags=true</td>
  </tr>
</table>

####Response fields

<table>
  <tr>
    <td>Array of <a href="image-object.md">image obj</a>'s</td>
  </tr>
</table>

**Note:** Currently there is no pagination implemented. The endpoint will return **all** images, no matter how many there are. This will change soon.

#### Examples
todo