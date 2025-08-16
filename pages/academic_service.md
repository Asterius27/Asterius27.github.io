---
layout: page
title: Academic Service
permalink: /academicservice/
weight: 5
---

<h2 class="mb-4">Academic Service</h2>

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
