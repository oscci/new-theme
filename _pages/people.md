---
title: "People"
tagline: "Find your key contacts"
description: Key people involved in ReproducibleResearchOxford
permalink: /people/
type: page
---

<div class="initial-content">
  {% for person in site.team %}
    <h2>{{ person.name }} - {{ person.position }}</h2>
    <p>{{ person.content | markdownify }}</p>
  {% endfor %}
</div>
