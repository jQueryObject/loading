# jquery页面loading提示用户等待效果loading
效果如下：
![](images/img.gif)

all code:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>jquery页面loading提示用户等待效果</title>
    <style>
        .mloadingDiv{
            position:absolute;
            left:0;
            width:100%;
            top:0;
            background:#f3f8ff;
            opacity:0.8;
            filter:alpha(opacity=90);
            z-index:10000;
        }
        .loadingDivChild{
            position: absolute;
            cursor: wait;
            width: auto;
            height:57px;
            line-height:57px;
            padding-left: 50px;
            padding-right: 5px;
            background: #fff url(images/gif.gif) no-repeat scroll 18px 20px;
            border: 2px solid #95B8E7;
            color: #696969;
            font-family:\'Microsoft YaHei\';
        }
    </style>
</head>
<body>
<div class="mloadingDiv">
    <div class="loadingDivChild">
        正在从数据库请求数据，请您耐心等候.............
    </div>
</div>
</body>
</html>
<script src="js/jquery-3.2.1.js"></script>
<script>
    // 定义mloadingDiv的宽高及其子元素
    $(".mloadingDiv").height(window.innerHeight);
    var _Top = window.innerHeight > 61 ? (window.innerHeight - 61) / 2 : 0,
            _Left = window.innerWidth > 215 ? (window.innerWidth - 215) / 2 : 0;
    $(".loadingDivChild").css({
        "left": _Left,
        "top": _Top
    });
</script>
```

