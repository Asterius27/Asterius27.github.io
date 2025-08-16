---
layout: page
title: Teaching
permalink: /teaching/
weight: 4
---

<h2 class="mb-4">Teaching Activity</h2>

<style>
.teaching-year {
  font-weight: 600;
  color: #0d6efd; /* Bootstrap blue */
  margin-top: 2rem;
  margin-bottom: 1rem;
  font-size: 1.2rem;
}
.teaching-item {
  display: flex;
  gap: 1rem;
  margin-bottom: 0.75rem;
}
.teaching-item .role-course {
  font-weight: 500;
}
.teaching-item small {
  color: #6c757d;
}
</style>

{% assign items = site.data.teaching.teaching | sort: "start" | reverse %}
{% assign current_year = "" %}

{% for t in items %}
  {% assign year = t.start | date: "%Y" %}
  {% if year != current_year %}
    <div class="teaching-year">{{ year }}</div>
    {% assign current_year = year %}
  {% endif %}

  <div class="teaching-item">
    <div class="role-course">
      <strong>{{ t.role }}</strong> — <em>{{ t.course }}</em>
    </div>
    <div>
      {% if t.professor %}{{ t.professor }}, {% endif %}{{ t.institution }}
      {% if t.hours != "" %} • {{ t.hours }} hours{% endif %}
    </div>
  </div>
{% endfor %}
