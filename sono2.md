# index.html
```html

<!DOCTYPE html>

<html lang="ja">

 <head>
  <title>my-blog</title>
  <script
  src="https://code.jquery.com/jquery-3.3.1.min.js"
  integrity="sha256-FgpCb/KJQlLNfOu91ta32o/NMZxltwRo8QtmkMRdAu8="
  crossorigin="anonymous"></script>
  <script src="index.js" type="text/javascript"></script>

  <link rel="stylesheet" type="text/css" href="index.css">
 </head>

<body>
  <div class="boss">
    <div class="hedder">
      <h1 class="title">検★証★</h1>
      <div class="flex-box">
        <a class="flex-boll">about</a>
        <a class="flex-boll">login</a>
        <a class="flex-boll">sign up</a>
        
      </div>
    </div>
   
    <div class="main">
      <p class="test">↓クリックしてください</p>
      <p id="con">ipadの特徴</p>
      
    </div>
    <div class="kashi">
      <br><br>
      <p>・パソコンと違い、小さい、軽い、低価格</p>
      <p>・実はプログラミングが出来る</p>
      <p>・スマホアプリが大画面で楽しめる</p>
    </div>
  </div>
</body>

</html>
```
# index.css
```css:index.css
.hedder{
  background-color: rgb(255, 178, 62);
  display: flex;/*横並びにする*/ 
  margin-bottom: 0;
}
h1{
  color:darkred;
}
.title{
  display: inline;
  margin: 0 0 auto 0;
  padding: 6px 10px;
}
body{
  background-color:#fff2db;

}
.main{
  background-color: floralwhite;
  width:600px;
  margin-left:100px;
}
.flex-box{
  margin: 0 0 0 500px;
  display: flex;/*横並びにする*/ 
  border-right: dashed 2px rgb(251, 255, 0);
}
.flex-boll{
  border-left: dashed 2px rgb(251, 255, 0);
  padding: 15px 5px 5px;
}
a{
  color: black;
}
#con{
  position:relative;
  z-index: 20;
}
.kashi{
  border-color: #d36015;
  background-color: #fda971;
  display:inline-block;
  padding: 0px 10px 0px 10px;
  margin-left: 100px;
  position: relative;
}
```
# index.js
```javascript
$(document).ready(function(){

  $("p").css("color", '#844500');
  $("p.test").css("color","blue");
  $(".kashi").hide();
  $('.test').on({
    'click':function(){
      $(this).text("クリックされました。");
    }
    
  });
  
  $('.title').on({
    'mouseenter':function(){
      $(this).css("background-color",'#d68000');
    },
    'mouseleave':function(){
      $(this).css("background-color",'rgb(255, 178, 62)');
    }
  });
  $('.flex-boll').on({
    'mouseenter':function () {
      $(this).css("background-color",'#d68000');
    },
    'mouseleave':function(){
      $(this).css("background-color",'rgb(255, 178, 62)');
    }
  });
  $('#con').on('click',function(){//conがクリックされると
    $('#con').animate({//animate使うときはposition:relative;必須！！
      'left':'300px'//conを右に移動
      
    });
    $('.kashi').show(1000);
    $('.kashi').css("z-index","10");
    $('.kashi').animate({
      'bottom':'50px',
      'left':'180px'
    });
  });
  
});
```
