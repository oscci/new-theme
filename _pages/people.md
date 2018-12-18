---
title: "People"
tagline: "Find your key contacts"
description: Key people involved in ReproducibleResearchOxford
permalink: /people/
type: page
---

<div class="initial-content card-columns d-flex flex-column" id="accordion">
  {% for person in site.team %}
    <div class="card" data-toggle="collapse" data-target="#{{- person.name | replace: " ", "" -}}-Detail" id="{{- person.name | replace: " ", "" -}}">
      <div class="card-body">
        <h4 class="card-title">
          <a name="{{- person.name | replace: " ", "" -}}">{{ person.name }}</a>
        </h4>
        <p>{{ person.position }}</p>
        {% for group in person.groups %}
          {% if forloop.first == true %}
            <div class="btn-group">
          {% endif %}
              <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#{{- group | replace: " ", "" -}}-Modal">{{ group }}</button>
          {% if forloop.last == true %}
            </div>
          {% endif %}
        {% endfor %}
        <div id="{{- person.name | replace: " ", "" -}}-Detail" class="collapse" data-parent="#accordion">
          <div class="panel-body">
            {{ person.content | markdownify }}
          </div>
        </div>
      </div>
    </div>
  {% endfor %}
</div>

{% assign groupArray = "a, b, c" | split: ", " %}
{% for person in site.team %}
  {% if forloop.first == true %}
    {% assign groupArray = person.groups %}
  {% else %}
    {% assign groupArray = groupArray | concat: person.groups %}
  {% endif %}
{% endfor %}
{% assign groupArray = groupArray | uniq %}

{% for g in groupArray %}
  {% include group_list group=g %}
{% endfor %}

<script>
  function popOff(hash) {}
  //   if(typeof hash === 'undefined')
  //     hash = window.location.hash;
  //   let target = document.querySelector(hash + '-Detail');
  //   let cards = document.querySelectorAll('.collapse');
  //   for(let i = 0; i < cards.length; i++) {
  //     if(cards[i] === target)
  //       cards[i].collapse("show");
  //     else
  //       cards[i].collapse("hide");
  //   }
  //   $('.modal').modal("hide");
  // }
  //
  // setTimeout(function() {
  //   if(window.location.hash.length)
  //     popOff();
  //   window.onhashchange = popOff();
  // }, 100);
</script>
