---
layout: default
title: home
---

# ledcoyote.com

musings, thoughts, and loosely held positions

## blog (recent)

<ul>
  {% for post in site.posts limit:10 %}
    <li>
      <a href="{{ post.url }}">{{ post.date | date: "%Y-%m-%d" }}: {{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

[all posts](/blog) ([atom](/feed.xml))

## rainbow

you wanna rainbow??!?1 [HERE](/rainbow), have a rainbow!

## optics

[here](/optics-simple-raytrace) to play with some lenses. sorry it's not very
user-friendly

## links

[github](https://github.com/ledcoyote)

[linkedin](https://www.linkedin.com/in/charlie-keith-013a6ba6/)

## contact

email me at me at ellie dee coyote dotcom or get in touch through das socials
