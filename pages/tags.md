---
layout: page
title: 标签
description: 人越学越觉得自己无知
keywords: 标签, Tags
comments: false
menu: 标签
permalink: /tags/
---

> 记多少命令和快捷键会让脑袋爆炸呢？

<ul class="listing">
{% for tags in site.tags %}
{% if tags.title != "Wiki Template" %}
<li class="listing-item"><a href="{{ tags.url }}">{{ tags.title }}</a></li>
{% endif %}
{% endfor %}
</ul>
