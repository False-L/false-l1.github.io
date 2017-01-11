---
layout: page
title: About
description: 少壮不努力，老大徒伤悲。
keywords: YL Lin
comments: true
menu: 关于
permalink: /about/
---
   年轻的时候多多努力！
   
   I'm waterserver!
   
## 坚信

* 知识改变人生
* 学习成就梦想

## 联系

* GitHub：[@false-l](https://github.com/false-l)
* 微博: [@waterserver](http://weibo.com/waterserver)

## Skill Keywords

#### Software Engineer Keywords
<div class="btn-inline">
    {% for keyword in site.skill_software_keywords %}
    <button class="btn btn-outline" type="button">{{ keyword }}</button>
    {% endfor %}
</div>

#### Mobile Developer Keywords
<div class="btn-inline">
    {% for keyword in site.skill_mobile_app_keywords %}
    <button class="btn btn-outline" type="button">{{ keyword }}</button>
    {% endfor %}
</div>

#### Windows Developer Keywords
<div class="btn-inline">
    {% for keyword in site.skill_windows_keywords %}
    <button class="btn btn-outline" type="button">{{ keyword }}</button>
    {% endfor %}
</div>
