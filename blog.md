---
layout: default
title: blog
---

# all blog posts

[atom](/feed.xml)

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.date | date: "%Y-%m-%d" }}: {{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

<nav>
  <a href="/">home</a>
</nav>
