---
title: Members
layout: collection
permalink: /people/
collection: people
entries_layout: grid
sort_by: weight
---

Lab members

<div class="grid">
  {% assign current_members = site.people | where: "member_status", "current" %}
  {% for member in current_members %}
    <div class="grid-item">
      <img src="{{ member.image.thumbnail }}" alt="{{ member.title }}">
      <h2>{{ member.title }}</h2>
      <p>{{ member.content }}</p>
    </div>
  {% endfor %}
</div>

## Past Members

<div class="grid">
  {% assign past_members = site.people | where: "member_status", "past" %}
  {% for member in past_members %}
    <div class="grid-item">
      <img src="{{ member.image.thumbnail }}" alt="{{ member.title }}">
      <h2>{{ member.title }}</h2>
      <p>{{ member.content }}</p>
    </div>
  {% endfor %}
</div>
