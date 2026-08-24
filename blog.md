---
layout: single
title: "Blog & Analysis"
permalink: /blog/
author_profile: true
---

<ul style="list-style-type: none; padding-left: 0;">
  {% for post in site.posts %}
    <li style="margin-bottom: 1.5rem; border-bottom: 1px solid #eee; padding-bottom: 1rem;">
      <span style="font-size: 0.85rem; color: #777;">{{ post.date | date: "%B %d, %Y" }}</span><br>
      <a href="{{ post.url | relative_url }}" style="font-size: 1.2rem; font-weight: bold; text-decoration: none;">
        {{ post.title }}
      </a>
      {% if post.excerpt %}
        <p style="font-size: 0.95rem; color: #555; margin-top: 0.3rem;">{{ post.excerpt | strip_html | truncate: 160 }}</p>
      {% endif %}
    </li>
  {% endfor %}
</ul>
