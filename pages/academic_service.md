---
layout: page
title: Academic Service
permalink: /academicservice/
weight: 5
---

<h2 class="mb-4">Academic Service</h2>

{% assign services = site.data.service | sort: 'year' | reverse %}

<ul class="list-unstyled">
{% for item in services %}
  <li class="mb-3">
    <strong>{{ item.year }} – {{ item.role }}:</strong> {{ item.description }}
  </li>
{% endfor %}
</ul>
