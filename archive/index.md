---
layout:  page
title: archive
description: 归档
---


> 生亦何欢，死亦何苦 <span style="float:right"><a href="/">☊</a></span>



<ul class="archive">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <li class="year">{{ y }}</li>
  {% endif %}
  <li class="item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
