---
layout: page
title: Blog
permalink: /blog/
---

# Blog Posts

Below are my latest articles and notes:

<ul>
  {% for post in site.posts %}
    <li>
      <span>{{ post.date | date: "%b %d, %Y" }}</span> — 
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
