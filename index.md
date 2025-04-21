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
<style>
html, body {
    margin: 0;
    background: #620286 !important;
    min-height: 100vh;
    background-image: none !important;
}
</style>