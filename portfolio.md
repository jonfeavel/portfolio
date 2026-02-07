---
layout: default
title: "Professional Portfolio"
permalink: /portfolio/
---

# My Technical Exemplars
Below is a collection of my strategy frameworks and data analysis projects.

{% for item in site.exemplars %}
  <div class="activity-card">
    <div class="icon-box">{{ item.type | slice: 0 | upcase }}</div>
    <div class="card-content">
      <a href="{{ item.url | relative_url }}"><h3>{{ item.title }}</h3></a>
      <p>{{ item.description }}</p>
    </div>
  </div>
{% endfor %}
