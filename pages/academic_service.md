---
layout: page
title: Academic Service
permalink: /academicservice/
weight: 5
---

<h2 class="mb-2">Academic Service</h2>

<div style="margin-bottom: 2rem;">
  <a href="https://orcid.org/0009-0009-1054-1234" target="_blank" rel="noopener" class="btn btn-outline-primary btn-sm me-2">
    ORCID
  </a>
  <a href="https://www.webofscience.com/wos/author/record/MCY-2623-2025" target="_blank" rel="noopener" class="btn btn-outline-info btn-sm">
    Web of Science
  </a>
</div>

{% assign services = site.data.service | group_by: 'year' | sort: 'name' | reverse %}

{% for group in services %}
  <h3 class="mt-4">{{ group.name }}</h3>
  <ul class="ps-3">
    {% for item in group.items %}
      <li class="mb-2">
        <strong>{{ item.role }}</strong> — {{ item.description }}
      </li>
    {% endfor %}
  </ul>
{% endfor %}
