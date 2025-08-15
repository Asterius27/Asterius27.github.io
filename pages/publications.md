---
layout: page
title: Publications
permalink: /publications/
weight: 2
---

<h2 class="mb-4">Publications</h2>

{% assign pubs_by_year = site.data.publications | sort: "year" | reverse | group_by: "year" %}

{% for year_group in pubs_by_year %}
  <h3 class="mt-4">{{ year_group.name }}</h3>
  
  {% for pub in year_group.items %}
    <div class="card mb-3 shadow-sm border-0">
      <div class="card-body">
        <h5 class="card-title mb-1">{{ pub.title }}</h5>
        <p class="card-text mb-1"><strong>Authors:</strong> {{ pub.authors }}</p>
        <p class="card-text"><em>{{ pub.venue }}</em>, {{ pub.year }}</p>
        <div>
          {% if pub.link %}
            <a href="{{ pub.link }}" target="_blank" class="btn btn-primary btn-sm me-2">
              Read Paper
            </a>
          {% endif %}
          {% if pub.code %}
            <a href="{{ pub.code }}" target="_blank" class="btn btn-outline-secondary btn-sm">
              View Code
            </a>
          {% endif %}
        </div>
      </div>
    </div>
  {% endfor %}
{% endfor %}
