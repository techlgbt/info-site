---
layout: default
title: Moderation Blog
permalink: /blog/
---

# Moderation Blog

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
