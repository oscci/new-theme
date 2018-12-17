---
title: "Events"
tagline: "What's going on in Oxford?"
description: Key reproducibility events in Oxford
type: page
header:
  image: /assets/images/about-us.png
permalink: /events/
---

<div class="initial-content">
  {% for event in site.events %}
    <h2>{{ event.title }} - {{ event.type }}</h2>
    <p>{{ event.content | markdownify }}</p>
  {% endfor %}
</div>
