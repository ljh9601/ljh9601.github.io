<!--
---
layout: category
title: '프로그래머스'
permalink: Algorithm/Programmers
---

<ul class="posts-list">  
  {% assign category = page.category | default: page.title %}
  <h4>Posts in {{ category }} ({{ site.categories[category].size }})</h4> 
  {% for post in site.categories[category] %}   
    <li>
      <a class="post-title" href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
      <small><time>
        {{ post.date | date:"%F" }} {{ post.date | date: "%a" }}.
      </time></small>
    </li>
  {% endfor %}
</ul>
-->
---
layout: default
---
<ul class="posts-list">  
  {% assign category = page.category | default: page.title %}
  <h4>categories in {{ category }} ({{ site.categories[category].size }})</h4> 
  {% for cate in site.categories[category] %}   
    <li>
      <a class="post-title" href="{{ site.baseurl }}{{ post.url }}">{{ cate.title }}</a>
    </li>
  {% endfor %}
</ul>