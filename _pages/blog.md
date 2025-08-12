---
title: "Blog"
permalink: /blog/
layout: single
entries_layout: grid
show_excerpts: true
---

## My Blog

<ul class="post-cards">
{% for post in site.posts %}
  <li class="post-card">
    <a href="{{ post.url | relative_url }}">
      {% if post.header and post.header.teaser %}
        <img src="{{ post.header.teaser | relative_url }}" alt="{{ post.title }} teaser">
      {% endif %}
      <h3>{{ post.title }}</h3>
      <p>{{ post.excerpt | strip_html | truncate: 140 }}</p>
    </a>
  </li>
{% endfor %}
</ul>