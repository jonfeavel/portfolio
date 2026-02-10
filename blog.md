---
layout: null
permalink: /blog/
---
<link rel="stylesheet" href="{{ '/style.css' | relative_url }}">

<div class="library-wrapper">

  <aside class="library-sidebar">
    <nav>
      <ul class="sidebar-nav">
        <li><a href="{{ '/' | relative_url }}">Home</a></li>
        <hr style="border: 0; border-top: 1px solid rgba(255,255,255,0.1); margin: 20px 0;">
        <li><a href="{{ '/portfolio/' | relative_url }}">Portfolio</a></li>
        <li><a href="{{ '/blog/' | relative_url }}" class="active">Blog</a></li>
        <li><a href="{{ '/contact/' | relative_url }}">Contact Me</a></li>
        <li><a href="{{ '/projects/' | relative_url }}">Side Projects</a></li>
      </ul>
    </nav>
  </aside>

  <main class="library-content">
    <h1>Blog</h1>

    <p class="subtitle">
      Below is a curated collection of perspectives and writing I’m putting together throughout my professional journey.
    </p>

    <hr style="border: 0; border-top: 1px solid rgba(255,255,255,0.1); margin: 30px 0;">

    <div class="activity-feed">
      {% for item in site.posts %}
        {% if item.categories contains 'blog' %}
          <div class="activity-card">
            <div class="icon-box">{{ item.type | slice: 0 | upcase }}</div>
            <div class="card-text">
              <h3><a href="{{ item.url | relative_url }}">{{ item.title }}</a></h3>
              <p>{{ item.description }}</p>
            </div>
          </div>
        {% endif %}
      {% endfor %}
    </div>
  </main>

</div>
