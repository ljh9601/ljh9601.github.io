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

<!--
{% assign date_format = site.date_format | default: "%B %-d, %Y" %}

<div id="full-tags-list">
    {%- assign category = page.title -%}
    <div class="post-list">
        {%- for post in site.categories[category] -%}
            <div class="tag-entry">
                <a href="{{ post.url | relative_url }}">{{- post.title -}}</a>
                <div class="entry-date">
                    <time datetime="{{- post.date | date_to_xmlschema -}}">{{- post.date | date: date_format -}}</time>
                </div>
            </div>
        {%- endfor -%}
    </div>
</div>
-->