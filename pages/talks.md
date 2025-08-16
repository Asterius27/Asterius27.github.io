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
  border-left: 2px solid #dee2e6;
  margin-left: 1rem;
  padding-left: 1.5rem;
}
.timeline::before {
  content: "";
  position: absolute;
  left: -7px;
  top: 0;
  bottom: 0;
  width: 14px;
  border-radius: 50%;
}
.timeline-item {
  position: relative;
  margin-bottom: 2rem;
}
.timeline-item::before {
  content: "";
  position: absolute;
  left: -23px;
  top: 6px;
  width: 12px;
  height: 12px;
  background-color: #0d6efd; /* Bootstrap primary */
  border-radius: 50%;
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