---
layout: home
---

> Welcome to onlymanes Blog! There lists my articles.

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

<link rel="stylesheet" href="{{ '/assets/css/custom.css' | relative_url }}">