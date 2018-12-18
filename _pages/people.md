---
title: "People"
tagline: "Find your key contacts"
description: Key people involved in ReproducibleResearchOxford
permalink: /people/
type: page
---

<div class="initial-content" id="accordion">
  {% for person in site.team %}
    <div class="panel panel-default">
      <h2 class="panel-title">
        <a data-toggle="collapse" data-parent="#accordion" data-target="#{{- person.name | replace: " ", "-" -}}" href="javascript:void(0);" name="{{- person.name | replace: " ", "" -}}">{{ person.name }}</a>
      </h2>
      <p>{{ person.position }}</p>
      <div id="{{- person.name | replace: " ", "-" -}}" class="panel-collapse collapse">
        <div class="panel-body">
          {{ person.content | markdownify }}
        </div>
      </div>
    </div>
  {% endfor %}
</div>
