---
layout: default
---

<div class="about-section">
  <p>
    &emsp;&emsp;> About me:
  <br>
  <br>&emsp;&emsp;- Name: Helen.Z
  <br>&emsp;&emsp;- I'm from Beijing, China and a permanent resident of Canada, living in Regina.
  <br>&emsp;&emsp;- My MBTI is INTJ, and my Constellation is Aquarius.
  <br>&emsp;&emsp;- My interests include music, singing, drawing, traveling, and many more!
  </p>
</div>

<div class="post-section">
  <p><br>&emsp;&emsp;> Welcome to onlymanes Blog! There lists my articles.</p>
  <ul class="post-list">
    {% for post in site.posts %}
      <li class="post-item">
        <a href="{{ post.url }}" class="post-link">{{ post.title }}</a>
      </li>
    {% endfor %}
  </ul>
</div>

<div class="visitor-counter">
  Total Visitors: <span id="visitorCount">Loading...</span>
</div>

<script src="https://www.gstatic.com/firebasejs/8.10.0/firebase-app.js"></script>
<script src="https://www.gstatic.com/firebasejs/8.10.0/firebase-database.js"></script>

<script>
  const firebaseConfig = {
  apiKey: "AIzaSyAETlOOjT2ulQn-JeUrNKdRMaYhR4o7D2k",
  authDomain: "onlymanes-blog.firebaseapp.com",
  projectId: "onlymanes-blog",
  storageBucket: "onlymanes-blog.firebasestorage.app",
  messagingSenderId: "888926945739",
  appId: "1:888926945739:web:094a1e33c1f01512bb364e",
  measurementId: "G-NVQPRSXNKM"
};
  
  firebase.initializeApp(firebaseConfig);
  
  document.addEventListener('DOMContentLoaded', () => {
    const db = firebase.database();
    const counterRef = db.ref('visitorCount');
    
    if (!sessionStorage.getItem('counted')) {
      counterRef.transaction(current => (current || 0) + 1);
      sessionStorage.setItem('counted', 'true');
    }

    counterRef.on('value', snapshot => {
      document.getElementById('visitorCount').textContent = snapshot.val();
    });
  });
</script>