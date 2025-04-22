---
layout: default
---

<div class="about-section">
  <p>
    &emsp;&emsp;> About me:
  <br><br>
  <br>&emsp;&emsp;- Name: Helen Z.
  <br>&emsp;&emsp;- I'm from Beijing, China and a permanent resident of Canada, living in Regina.
  <br>&emsp;&emsp;- My MBTI is INTJ, and my Constellation is Aquarius.
  <br>&emsp;&emsp;- My interests include music, singing, drawing, traveling, and many more!
  </p>
</div>

<div class="post-section">
  <p>&emsp;&emsp;> Welcome to onlymanes Blog! There lists my articles.</p>
  <ul class="post-list">
    {% for post in site.posts %}
      <li class="post-item">
        <a href="{{ post.url }}" class="post-link">{{ post.title }}</a>
      </li>
    {% endfor %}
  </ul>
</div>


<div class="content-container">
    <div class="main-layout">
        <div class="text-section">
            <!-- ÄãµÄÎÄ×ÖÄÚÈÝ -->
        </div>
        
        <div class="cover-wrapper">
            <div class="cover-image"></div>
            <div class="watermark-circle">only<br>manes</div>
        </div>
    </div>
</div>