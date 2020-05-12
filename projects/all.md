---
layout: default
---

<!-- Note to self: Finally made this page "dynamic" :P -->

{% assign proj_sorted = site.projects | sort: 'rank' %}
{% for proj in proj_sorted %}
  <div>
    <h1 class="maintitle">{{ proj.title }}</h1>
    <h3 class="subtitle">
      {% if proj.awards == nil %}
        {{ proj.time }}
      {% else %}
        {{ proj.time }}, {{ proj.awards }}
      {% endif %}
      <!-- {{proj.time}}, {{ proj.awards }} -->
    </h3>
    <h3>{{ proj.description }}</h3>

    <p>{{ proj.content | markdownify }}</p>
  </div>
  {% if forloop.index < proj_sorted.size %}<hr>{% endif %}
{% endfor %}
