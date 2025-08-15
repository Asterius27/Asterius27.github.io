---
layout: page
title: Publications
permalink: /publications/
weight: 2
---

<h2 class="mb-4">Publications</h2>

{% assign groups = site.data.publications | group_by: 'year' | sort: 'name' | reverse %}

{% for group in groups %}
<h3 class="mt-4">{{ group.name }}</h3>

{% for pub in group.items %}
<div class="card mb-3 shadow-sm border-0">
  <div class="card-body d-flex flex-column flex-md-row align-items-md-center justify-content-between gap-2">
    <div class="me-md-3">
      <h5 class="card-title mb-1">{{ pub.title }}</h5>
      <p class="mb-1"><strong>Authors:</strong> {{ pub.authors }}</p>
      <p class="mb-0"><em>{{ pub.venue }}</em></p>
    </div>

    <div class="mt-2 mt-md-0 text-nowrap">
      {% if pub.link %}
        <a href="{{ pub.link }}" target="_blank" rel="noopener" class="btn btn-primary btn-sm me-2">Read Paper</a>
      {% endif %}
      {% if pub.code %}
        <a href="{{ pub.code }}" target="_blank" rel="noopener" class="btn btn-outline-secondary btn-sm">View Code</a>
      {% endif %}
    </div>
  </div>
</div>
{% endfor %}
{% endfor %}
