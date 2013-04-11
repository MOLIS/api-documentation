`http://api.molis.io/v1/image`

Upload a file.

* HTTP method: POST (multipart/form-data)
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
The endpoint expects an array of objects with the following fields:

<table>
  <tr>
    <td>Name</td>
    <td>Description</td>
    <td>Type</td>
    <td>Example / possible value</td>
  </tr>
  <tr>
    <td>file</td>
    <td><strong>required</strong> Image file</td>
    <td></td>
    <td></td>
  </tr>
</table>


#### Response fields
An <a href="image-object.md">image object</a>'s.