---
layout: null
title: Home
---
<link rel="stylesheet" href="{{ '/style.css' | relative_url }}">

<div class="landing-container">

  <header class="hero-box">
    <img src="{{ '/assets/Head-shot-icon.PNG' | relative_url }}" class="profile-pic" alt="J. Feavel">
    <div class="hero-text">
      <h1>J Feavel</h1>
      <h3>Simplifying Complexity as AI Terraforms the Tech Industry</h3>
      <p>I believe AI is terraforming the tech industry, shifting the advantage toward those with a diversified technical acumen and an uncompromising focus on outcomes. My mission is to make the complex simple.</p>
    </div>
  </header>

  <nav class="pillar-grid">
    <a href="{{ '/portfolio/' | relative_url }}" class="pillar">Portfolio</a>
    <a href="{{ '/blog/' | relative_url }}" class="pillar">Blog</a>
    <a href="{{ '/contact/' | relative_url }}" class="pillar secondary">Contact</a>
    <a href="{{ '/projects/' | relative_url }}" class="pillar secondary">Side Projects</a>
  </nav>

  <h2 class="recent-activity-header">Recent Activity</h2>
  
  <div class="activity-feed">
    {% for item in site.posts limit:5 %}
    <div class="activity-card">
      <div class="icon-box">{{ item.type | slice: 0 | upcase }}</div>
      <div class="card-text">
        <h3><a href="{{ item.url | relative_url }}">{{ item.title }}</a></h3>
        <p>{{ item.description }}</p>
      </div>
    </div>
    {% endfor %}
  </div>

</div>
