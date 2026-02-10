---
layout: null
permalink: /portfolio/
---
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portfolio | Jon Feavel</title>
  <link rel="stylesheet" href="{{ '/style.css' | relative_url }}">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
</head>
<body>

<div class="library-wrapper">

  <aside class="library-sidebar">
    <nav>
      <ul class="sidebar-nav">
        <li><a href="{{ '/' | relative_url }}" class="nav-back">← Home</a></li>
        
        <hr style="border: 0; border-top: 1px solid rgba(255,255,255,0.1); margin: 20px 0;">
        
        <li><a href="{{ '/portfolio/' | relative_url }}" class="nav-prominent active">Portfolio</a></li>
        <li><a href="{{ '/blog/' | relative_url }}" class="nav-prominent">Blog</a></li>
        
        <li><a href="{{ '/projects/' | relative_url }}">Side Projects</a></li>
        <li><a href="{{ '/contact/' | relative_url }}">Contact Me</a></li>
      </ul>
    </nav>
  </aside>

  <main class="library-content">
    <h1>Portfolio</h1>
    
    <p class="subtitle">Below is a curated collection of <strong>select work from my professional journey</strong>. From coursework, to research, or custom framework creation, each piece is presented in a way that feels as though we were sitting across from one another in a meeting room.</p>

    <hr style="border: 0; border-top: 1px solid rgba(255,255,255,0.1); margin: 30px 0;">

    <div class="activity-feed">
      {% for item in site.portfolio %}
        <div class="activity-card">
          <div class="icon-box">
            {{ item.title | slice: 0 | upcase }}
          </div>
          
          <div class="card-text">
            <h3><a href="{{ item.url | relative_url }}">{{ item.title }}</a></h3>
            <p>{{ item.description }}</p>
          </div>
        </div>
      {% endfor %}
    </div>
  </main>

</div>

</body>
</html>
