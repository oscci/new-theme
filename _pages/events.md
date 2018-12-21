---
title: "Events"
tagline: "What's going on in Oxford?"
description: Key reproducibility events in Oxford
type: page
permalink: /events/
---

<div class="initial-content" id="accordion">
  {% for event in site.events %}
    <div class="card event">
      <div class="card-header" data-toggle="collapse" data-target="#{{- event.title | replace: " ", "" -}}">
        <h4>{{ event.title }}</h4>
        <p>{{ event.type }}</p>
      </div>
      <div class="card-body collapse" id="{{- event.title | replace: " ", "" -}}" data-parent="#accordion">
        <div class="event-detail">
          {{ event.content | markdownify }}
        </div>
        <div class="event-people">
          {% assign people = site.team | sort_natural: 'lastname' %}
          {% for person in people %}
            {% if person.groups contains event.title %}
              <div class="btn btn-outline-info" onclick="window.location.assign('{{ '/people' | relative_url }}#{{- person.firstname | append: person.lastname | replace: ' ', '' -}}')">
                {{ person.firstname }} {{ person.lastname }}
              </div>
            {% endif %}
          {% endfor %}
        </div>
      </div>
    </div>
  {% endfor %}
</div>

{% include scrollToId.html %}
