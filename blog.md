---
layout: single
title: "Blog & Analysis"
permalink: /blog/
author_profile: true
sidebar:
  nav: "main"
---
Below you'll find my latest essays, research notes, and policy analyses.
---
<ul style="list-style-type: none; padding-left: 0;">
  {% for post in site.posts %}
    <li style="margin-bottom: 1.5rem; border-bottom: 1px solid #eee; padding-bottom: 1rem;">
      <span style="font-size: 0.85rem; color: #777;">{{ post.date | date: "%B %d, %Y" }}</span><br>
      <a href="{{ post.url | relative_url }}" style="font-size: 1.25rem; font-weight: bold; text-decoration: none;">
        {{ post.title }}
      </a>
      {% if post.excerpt %}
        <p style="font-size: 0.95rem; color: #555; margin-top: 0.4rem;">
          {{ post.excerpt | strip_html | truncate: 160 }}
        </p>
      {% endif %}
    </li>
  {% else %}
    <p><em>No posts published yet.</em></p>
  {% endfor %}
</ul>
