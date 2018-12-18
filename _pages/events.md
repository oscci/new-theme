---
title: "Events"
tagline: "What's going on in Oxford?"
description: Key reproducibility events in Oxford
type: page
header:
  image: /assets/images/about-us.png
permalink: /events/
---

<div class="initial-content" id="accordion">
  {% for event in site.events %}
    <div class="panel panel-default">
      <h2 class="panel-title">
        <a data-toggle="collapse" data-parent="#accordion" data-target="#{{- event.title | replace: " ", "-" -}}" href="javascript:void(0);" id="{{- event.title | replace: " ", "" -}}">{{ event.title }} - {{ event.type }}</a>
      </h2>
      <div id="{{- event.title | replace: " ", "-" -}}" class="panel-collapse collapse
      {% if forloop.first == true %}
       show
     {% endif %}">
        <div class="panel-body">
          {{ event.content | markdownify }}
        </div>
      </div>
    </div>
  {% endfor %}
</div>
