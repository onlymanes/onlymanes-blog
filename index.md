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

body::before {
    content: "";
    position: fixed;
    right: 0;
    top: 50%;
    transform: translateY(-50%);
    width: 60vw;
    height: 70vh;
    background:
        linear-gradient(to left, rgba(16,0,22,0) 0%, rgba(16,0,22,1) 70%),
        url("/assets/img/cover.jpg");
    background-repeat: no-repeat;
    background-position: right center;
    background-size: cover;
    z-index: -1;
    pointer-events: none;
    border-radius: 8px 0 0 8px;
}

/* Debugging: Add a solid color to see if the pseudo-element is present */
body::after {
    content: "Debug";
    position: fixed;
    bottom: 10px;
    right: 10px;
    background-color: white;
    color: black;
    padding: 5px;
    font-size: 14px;
    z-index: 1000;
}

.rss-subscribe, .feed-subscribe {
    display: none !important;
    visibility: hidden !important;
}

.main-content {
    position: relative;
    z-index: 1;
    background: transparent !important;
}
</style>

{% include footer.html %}