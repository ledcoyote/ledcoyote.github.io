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

🌈🌈🌈 you wanna rainbow??!?1 [HERE](/rainbow), have a rainbow! 🌈🌈🌈

## optics

![Image]({{ "/assets/images/lens_system.png" | relative_url }}){: width="250" }

[here](/optics-simple-raytrace) to play with some lenses. it's not super
user-friendly, but it's kinda fun.

## links

- [github](https://github.com/ledcoyote)
- [bluesky](https://bsky.app/profile/ledcoyote.bsky.social)
- [linkedin](https://www.linkedin.com/in/charlie-keith-013a6ba6/)

## contact

if you have anything interesting you think i should know about feel free to email me at my first name at ellie dee coyote dotcom.
