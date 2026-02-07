---
layout: default
title: "Professional Portfolio"
permalink: /portfolio/
---

# Professional Portfolio
See below for additions to my professional portfolio. 

{% for item in site.exemplars %}
  <div class="activity-card">
    <div class="icon-box">D</div>
    <div class="card-content">
      <a href="{{ item.url | relative_url }}"><h3>{{ item.title }}</h3></a>
      <p>{{ item.description }}</p>
    </div>
  </div>
{% endfor %}
