---
layout: home
author_profile: true
---

<!-- Intro Section -->
<section class="intro">
  <img src="assets/Profile.png" alt="Profile picture of Rica Esquivel" class="profile-pic">
  <div class="intro-text">
    <h1>Rica Esquivel</h1>
    <p>Hello, I'm Rica – a Computer Science undergraduate at Virginia Tech, graduating in December 2025. I've interned in data science and machine learning roles at Tractor Supply Company and HII Mission Technologies, applying my skills in Python, SQL, Java, R, and C. I'm experienced in machine learning, natural language processing (NLP), and working with cloud/data platforms like Snowflake and AWS.</p>
    <div class="button-group">
      <a href="https://www.linkedin.com/in/rica-esquivel/" target="_blank" class="btn">LinkedIn</a>
      <a href="assets/Rica_Esquivel_Resume.pdf" 
      target="_blank" class="btn">View Resume</a>
      <a href="https://www.goodreads.com/user/show/188499200-rica-esquivel" target="_blank" class="btn>GoodReads</a>
    </div>
  </div>
</section>

---

## Explore My Portfolio
<div class="cards">
  <a class="card" href="{{ '/cadets/' | relative_url }}">Corps of Cadets</a>
  <a class="card" href="{{ '/internships-tractor/' | relative_url }}">Internship: Tractor Supply</a>
  <a class="card" href="{{ '/internships-hii/' | relative_url }}">Internship: HII Mission Technologies</a>
  <a class="card" href="{{ '/projects/' | relative_url }}">Technical Projects</a>
  <a class="card" href="{{ '/goals/' | relative_url }}">Goals & Specialization</a>
  <a class="card" href="{{ '/blog/' | relative_url }}">Blog</a>
</div>

<!-- ### Recent Posts
<div class="post-previews">
{% for post in site.posts limit:3 %}
  <a class="post-preview" href="{{ post.url | relative_url }}">
    {% if post.header and post.header.teaser %}
      <img src="{{ post.header.teaser | relative_url }}" alt="{{ post.title }} teaser">
    {% endif %}
    <h3>{{ post.title }}</h3>
    <p class="meta">{{ post.date | date: "%B %d, %Y" }}</p>
    <p>{{ post.excerpt | strip_html | truncate: 140 }}</p>
  </a>
{% endfor %}
</div>
<p><a class="btn" href="{{ '/blog/' | relative_url }}">View all posts →</a></p> -->