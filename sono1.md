# index.html

```html
<!DOCTYPE html>

<html lang="ja">

 <head>
  <title>my-blog</title>
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
    </div>
</body>

</html>
```
# index.css
```css
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
.flex-box{
  margin: 0 0 0 500px;
  display: flex;/*横並びにする*/ 
  border-right: dashed 2px rgb(251, 255, 0);
}
.flex-boll{
  border-left: dashed 2px rgb(251, 255, 0);
  padding: 15px 5px 5px;
}
```
