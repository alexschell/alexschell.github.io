---
layout: default
title: Home
permalink: /
---

# Alex Schell's Homepage

Hi there.

## Recent posts

<ul class="post-list">
  {% for post in site.posts limit:5 %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span class="date">{{ post.date | date: "%b %Y" }}</span>
    </li>
  {% endfor %}
</ul>

[All posts →]({{ '/blog/' | relative_url }})
