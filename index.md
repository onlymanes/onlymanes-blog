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

<style>
html, body {
    margin: 0;
    min-height: 100vh;
}
</style>