---
layout: default
title: home
---

# ledcoyote.com

musings, thoughts, and loosely held positions

## links

[github](https://github.com/ledcoyote)

## blog

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.date | date: "%Y-%m-%d" }}: {{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
