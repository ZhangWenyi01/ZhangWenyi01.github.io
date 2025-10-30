---
layout: default
title: Home
---

# Welcome to {{ site.title }}

<ul class="posts">
{% for post in site.posts %}
  {% unless post.published == false %}
  <li class="post-item">
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="post-date">{{ post.date | date: "%Y-%m-%d" }}</span>
  </li>
  {% endunless %}
{% endfor %}
</ul>
