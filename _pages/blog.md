---
title: "Blog"
permalink: /blog/
layout: single
---

## My Blog

<ul>
{% for post in site.posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a> – {{ post.date | date: "%B %d, %Y" }}
  </li>
{% endfor %}
</ul>