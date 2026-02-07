---
layout: default
title: "Perspectives Blog"
---

# Perspectives
Reflections on AI, product strategy, and the shifting tech landscape.

{% for post in site.posts %}
  <div class="activity-card">
    <div class="icon-box">B</div>
    <div class="card-content">
      <a href="{{ post.url | relative_url }}"><h3>{{ post.title }}</h3></a>
      <p>{{ post.description }}</p>
    </div>
  </div>
{% endfor %}
