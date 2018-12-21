---

type: page
permalink: /all_groups

---
{% comment %} Iterate through people and build a list of groups {% endcomment %}
{% assign groupArray = "a, b, c" | split: ", " %}

{% for person in site.team %}

  {% if forloop.first == true %}
    {% assign groupArray = person.groups %}
  {% else %}
    {% assign groupArray = groupArray | concat: person.groups %}
  {% endif %}
{% endfor %}
{% assign groupArray = groupArray | uniq %}

{% comment %} List each group and the people in it {% endcomment %}

{% for group in groupArray %}
  <div class="card group-list">
    <div class="card-header" data-toggle="collapse" data-target="#{{ group }}"><a href="{{ '/' | relative_url }}events/#{{- group | replace: " ", "" -}}">{{ group }}</a></div>
    <div class="card-body collapse" id="{{ group }}">
      {% for person in site.team %}
        {% if person.groups contains group %}
          <a href="{{ '/' | relative_url }}people/#{{- person.name | replace: " ", "" -}}">
            <button type="button" class="btn btn-block">
              {{ person.name }}
            </button>
          </a>
        {% endif %}
      {% endfor %}
    </div>
  </div>
{% endfor %}
