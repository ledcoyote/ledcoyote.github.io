---
layout: default
title: home
---

# ledcoyote.com

musings, thoughts, and loosely held positions

## essays

<ul>
  <li>
    coming soon!
  </li>
</ul>

## blog

([rss/atom](/feed.xml))

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.date | date: "%Y-%m-%d" }}: {{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

## links

- [github](https://github.com/ledcoyote)
- [bluesky](https://bsky.app/profile/ledcoyote.bsky.social)

## contact

if you have anything interesting you think i should know about feel free to
email me at my first name at ellie dee coyote dotcom.
