---
title: "Events"
tagline: "What's going on in Oxford?"
description: Key reproducibility events in Oxford
type: page
permalink: /events/
---
---
<div class="initial-content" id="accordion">
  {% for event in site.events %}
    <div class="card event">
      <div class="card-header" data-toggle="collapse" data-target="#{{- event.title | replace: " ", "" -}}">
        {% if event.image_src %}
          <div class="logo">
            <img src="{{ 'assets/images/events' | relative_url}}/{{ event.image_src }}"/>
          </div>
        {% endif %}
        <div class="brief">
          <p class="text-muted">{{ event.type }}</p>
          <h4>{{ event.title }}</h4>
        </div>
      </div>
      <div class="card-body collapse" id="{{- event.title | replace: " ", "" -}}" data-parent="#accordion">
        <div class="card-links">
          <ul class="border-left border-muted">
          {% if event.website %}
            <li><i class="fa fa-globe" aria-hidden="true"></i><a href="{{ event.website }}">Event website</a></li>
          {% endif %}
          {% if event.twitter %}
            <li><i class="fab fa-fw fa-twitter-square" aria-hidden="true"></i><a href="https://twitter.com/{{ event.twitter }}">@{{ event.twitter }}</a></li>
          {% endif %}
          {% if event.soundcloud %}
            <li><i class="fab fa-soundcloud"></i><a href="https://soundcloud.com/{{ event.soundcloud }}">Soundcloud</a></li>
          {% endif %}
          </ul>
        </div>
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
