---
layout: page
title: Teaching
permalink: /teaching/
weight: 4
---

<h2 class="mb-4">Teaching Activity</h2>

<style>
.teaching-list dt {
  font-weight: 600;
  color: #0d6efd; /* Bootstrap blue */
  margin-top: 1rem;
}
.teaching-list dd {
  margin-bottom: 1rem;
  margin-left: 0;
  padding-left: 1rem;
  border-left: 2px solid #dee2e6;
}
.teaching-list em {
  color: #6c757d;
}
.teaching-list .small {
  color: #6c757d;
}
</style>

<dl class="teaching-list">
  {% assign items = site.data.teaching.teaching | sort: "start" | reverse %}
  {% for t in items %}
    <dt>{{ t.start | date: "%Y" }}</dt>
    <dd>
      <strong>{{ t.role }}</strong> — <em>{{ t.course }}</em><br>
      {% if t.professor %}{{ t.professor }}, {% endif %}{{ t.institution }}
      {% if t.hours != "" %} • {{ t.hours }} hours{% endif %}
    </dd>
  {% endfor %}
</dl>
