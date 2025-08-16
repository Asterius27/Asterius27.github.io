---
layout: page
title: Talks
permalink: /talks/
weight: 3
---

<h2 class="mb-4">Talks</h2>

<style>
.timeline {
  position: relative;
  border-left: 2px solid #dee2e6; /* the white/gray line */
  margin-left: 1rem;
  padding-left: 1.5rem;
}

.timeline-item {
  position: relative;
  margin-bottom: 2rem;
}

.timeline-item::before {
  content: "";
  position: absolute;
  left: -7px; /* centers the dot on the 2px line */
  top: 6px;
  width: 14px;
  height: 14px;
  background-color: #0d6efd; /* Bootstrap primary blue */
  border-radius: 50%;
  border: 2px solid #fff; /* makes the dot pop */
  box-shadow: 0 0 0 2px #dee2e6; /* optional, to blend with line */
}
</style>

<h3 class="mt-4">Conference Talks</h3>
<div class="timeline">
  {% assign confs = site.data.talks.conferences | sort: "date" | reverse %}
  {% for talk in confs %}
    <div class="timeline-item">
      <div class="fw-bold">{{ talk.title }}</div>
      <div class="text-muted small">
        {{ talk.venue }} — {{ talk.location }}  
        ({{ talk.date | date: "%B %-d, %Y" }})
      </div>
    </div>
  {% endfor %}
</div>

<h3 class="mt-4">Seminar Talks</h3>
<div class="timeline">
  {% assign sems = site.data.talks.seminars | sort: "date" | reverse %}
  {% for talk in sems %}
    <div class="timeline-item">
      <div class="fw-bold">{{ talk.title }}</div>
      <div class="text-muted small">
        {{ talk.venue }} — {{ talk.location }}  
        ({{ talk.date | date: "%B %-d, %Y" }})
      </div>
    </div>
  {% endfor %}
</div>