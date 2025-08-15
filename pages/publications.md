---
layout: page
title: Publications
permalink: /publications/
weight: 2
---

<h2 class="mb-4">Publications</h2>

<div class="row">
  {% for pub in site.data.publications %}
  <div class="col-lg-4 col-md-6 mb-4">
    <div class="card h-100 shadow-sm border-0">
      <div class="card-body d-flex flex-column">
        <h5 class="card-title">{{ pub.title }}</h5>
        <p class="card-text mb-2"><strong>Authors:</strong> {{ pub.authors }}</p>
        <p class="card-text mb-2"><em>{{ pub.venue }}</em>, {{ pub.year }}</p>

        <div class="mt-auto">
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
  </div>
  {% endfor %}
</div>
