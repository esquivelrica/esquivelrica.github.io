---
layout: home
author_profile: false
title: ""
header: false
---

<!-- Intro Section -->
<section class="intro">
  <img src="assets/Profile.png" alt="Profile picture of Rica Esquivel" class="profile-pic">
  
  <div class="intro-text">
    <h1>Rica Esquivel</h1>
    <p>Hello, I'm Rica – a Computer Science undergraduate at Virginia Tech, graduating in December 2025. I've interned in data science and machine learning roles at Tractor Supply Company and HII Mission Technologies, applying my skills in Python, SQL, Java, R, and C. I'm experienced in machine learning, natural language processing (NLP), and working with cloud/data platforms like Snowflake and AWS.</p>
    <div class="button-group">
      <a href="https://www.linkedin.com/in/rica-esquivel/" target="_blank" class="btn">LinkedIn</a>
      <a href="{{ '/assets/Rica_Esquivel_Resume.pdf' | relative_url }}" target="_blank" class="btn">View Resume</a>
      <a href="https://github.com/esquivelrica" target="_blank" class="btn">GitHub</a>
      <a href="https://www.goodreads.com/user/show/188499200-rica-esquivel" target="_blank" class="btn">Goodreads</a>
    </div>
  </div>
</section>

---

## Explore My Portfolio
<div class="cards">
  <a class="card" href="{{ '/cadets/' | relative_url }}">
    <i class="fas fa-shield-halved"></i>
    Corps of Cadets
  </a>
  <a class="card" href="{{ '/internships-tractor/' | relative_url }}">
    <i class="fas fa-store"></i>
    Internship: Tractor Supply
  </a>
  <a class="card" href="{{ '/internships-hii/' | relative_url }}">
    <i class="fas fa-ship"></i>
    Internship: HII Mission Technologies
  </a>
  <a class="card" href="{{ '/projects/' | relative_url }}">
    <i class="fas fa-code"></i>
    Technical Projects
  </a>
  <a class="card" href="{{ '/goals/' | relative_url }}">
    <i class="fas fa-bullseye"></i>
    Goals & Specialization
  </a>
  <a class="card" href="{{ '/blog/' | relative_url }}">
    <i class="fas fa-pen-nib"></i>
    Blog
  </a>
</div>

## Beyond the Office
<div class="beyond-office">
  <div class="hobby">
    <img src="{{ '/assets/hobbies/hiking.jpg' | relative_url }}" alt="Hiking trail view">
    <h3>Hiking</h3>
    <p>I love exploring trails and connecting with nature, from local paths to challenging summits.</p>
  </div>
  <div class="hobby">
    <img src="{{ '/assets/hobbies/fitness.jpg' | relative_url }}" alt="Weights and gym equipment">
    <h3>Fitness</h3>
    <p>Personal fitness is my way of staying focused, energized, and balanced in life.</p>
  </div>
  <div class="hobby">
    <img src="{{ '/assets/hobbies/cooking.jpg' | relative_url }}" alt="A plated meal">
    <h3>Cooking</h3>
    <p>In my kitchen, I experiment with recipes and flavors, making meals for friends and family.</p>
  </div>
</div>

<p style="text-align:center; margin-top:1rem;">
  <a href="{{ '/beyond-the-office/' | relative_url }}" class="btn">Learn More →</a>
</p>

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