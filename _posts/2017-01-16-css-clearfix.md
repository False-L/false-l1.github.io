---
layout: post
title: 清除浮动
description: "网站的浮动清除技术十分必要"
categories: [css]
keywords: Css
tags: 
      -[其他]
      -programmer
      -life goal
image:
  background: triangular.png
---
<h1>清除浮动</h1>
<p>如果父元素容器里面的子元素是浮动元素的话，我们一般需要在父元素闭合前
添加一个clear:both的元素用于清除浮动从而能使父容器正常被子元素内容撑起，
但是这种方法引入了多余的无意义标签，并且有javascript操作子元素的时候容易引发bug。
一种更好的方法是利用CSS，所以在一些CSS文件中经常会看到类似于.clearfix这样的类出没，
只要在父容器上应用这个类即可实现清除浮动。</p>
<h3>第一种方式：</h3>
<p>clearfix类，目前主流的清除浮动的方式。
<pre>
/* For modern browsers */
.clearfix:before,
.clearfix:after {
    content:"";
    display:table;
}

.clearfix:after {
    clear:both;
}

/* For IE 6/7 (trigger hasLayout) */
.clearfix {
    zoom:1;
}
</pre>
<h3>第二种方式：</h3>
overflow:hidden;
原理：父类会触发了BFC(block formatting context)块级格式化上下文，父类元素
不推荐。
<h3>第三种方式：</h3>
clear:both;
<p>在父类元素添加一个非浮动的空div，父类就会把</p>

