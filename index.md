---
layout: home
---

> Welcome to onlymanes Blog！Here lists my articles.

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

include:
  - assets/img/cover.jpg

<link rel="stylesheet" href="{{ '/assets/css/custom.css' | relative_url }}">

<p style="text-align:center;color:#666;margin:2rem 0;">
    &copy; onlymanes
</p>