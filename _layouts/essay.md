---
layout: default
---

<header>
  <h1>{{ page.title }}</h1>
  <p>by {{ page.author }}</p>
</header>

{{ content }}

<footer>
  {% if page.location %}
    <em>{{ page.location }}</em><br/>
  {% endif %}
  <em>{{ page.date | date: "%Y-%m-%d" }}</em>
</footer>

<nav>
  <ul>
    <li><a href="/">home</a></li>
  </ul>
</nav>
