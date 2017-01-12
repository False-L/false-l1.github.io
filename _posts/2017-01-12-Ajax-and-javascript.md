---
layout: post
title: 第一个Ajax调用
categories: [Ajax, JavaScript]
description: 本次尝试首先是在php+mysql+Apache环境下，通过javascript实现Ajax例子。
keywords: Ajax, JavaScript, Apache, php, mysql
---
#第一个Ajax调用
第一个Ajax调用：
本次尝试首先是在php+mysql+Apache环境下，通过javascript实现Ajax例子。
以下是html的代码  \n\n
核心为代码中js部分
```js
<script type="text/javascript">
function Ajax(){
var xmlHttpReq= null;
if(window.ActiveXObject){
xmlHttpReq =new ActiveXObject("Microsoft.XMLHTTP");
}else if(window.XMLHttpRequest){
xmlHttpReq =new XMLHttpRequest();
				}
if(xmlHttpReq != null){
xmlHttpReq.open("GET","test.php",true);
xmlHttpReq.onreadystatechange= RequestCallBack;
xmlHttpReq.send(null);
				}
function RequestCallBack(){
if(xmlHttpReq.readyState == 4){
if(xmlHttpReq.status == 200){
document.getElementById("resText").innerHTML =xmlHttpReq.responseText;
			}
		}
	}
}
</script>
```
以下是html的完成代码
```html
<!DOCTYPE HTML>
<html>
<head>
    <meta charset="utf-8">
<title>Ajax测试页</title>
<script type="text/javascript">
function Ajax(){
var xmlHttpReq= null;
if(window.ActiveXObject){
xmlHttpReq =new ActiveXObject("Microsoft.XMLHTTP");
}else if(window.XMLHttpRequest){
xmlHttpReq =new XMLHttpRequest();
				}
if(xmlHttpReq != null){
xmlHttpReq.open("GET","test.php",true);
xmlHttpReq.onreadystatechange= RequestCallBack;
xmlHttpReq.send(null);
				}
function RequestCallBack(){
if(xmlHttpReq.readyState == 4){
if(xmlHttpReq.status == 200){
document.getElementById("resText").innerHTML =xmlHttpReq.responseText;
			}
		}
	}
}
</script>
<style type="text/css">
</style>
</head>
<body>
	<input type="button" value="Ajax提交" onclick="Ajax();" />
	<div id="resText"></div>
</body>
```
#PHP代码
php代码较为简单,保存为text.php
```
<?php
echo "hello Ajax!";
?>
```