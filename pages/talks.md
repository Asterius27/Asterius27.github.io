---
layout: page
title: Talks
permalink: /talks/
weight: 3
---

<h2 class="mb-4">Talks</h2>

<div class="border-start ps-3">

  <h3 class="mt-4">Conference Talks</h3>
  {% for talk in site.data.talks.conferences %}
    <div class="mb-4">
      <div class="fw-bold">{{ talk.title }}</div>
      <div class="text-muted small">
        {{ talk.venue }} — {{ talk.location }}  
        ({{ talk.date | date: "%B %-d, %Y" }})
      </div>
    </div>
  {% endfor %}

  <h3 class="mt-4">Seminar Talks</h3>
  {% for talk in site.data.talks.seminars %}
    <div class="mb-4">
      <div class="fw-bold">{{ talk.title }}</div>
      <div class="text-muted small">
        {{ talk.venue }} — {{ talk.location }}  
        ({{ talk.date | date: "%B %-d, %Y" }})
      </div>
    </div>
  {% endfor %}

</div>