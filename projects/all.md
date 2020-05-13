---
layout: default
---

<!-- Note to self: Finally made this page "dynamic" :P -->

# Project Gallery

{% assign proj_sorted = site.projects | sort: 'rank' %}
<div class="card-group">
  {% for proj in proj_sorted %}
    <div class="card"  onclick="location.href='{{ proj.url }}#title';" style="cursor: pointer;">
      <img class="card-img-top" src="{{ proj.thumbnail }}" alt="Card image">

      <div class="card-body">
        <h2 class="card-title">{{ proj.title }}</h2>
        <p class="card-text">{{ proj.description }}</p>
      </div>
      <div class="card-footer">
        <small class="text-muted">{{ proj.time }}</small>
      </div>
    </div>
  {% endfor %}
</div>
