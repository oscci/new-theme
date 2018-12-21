---

type: page
permalink: /all_affiliations

---
{% comment %} Iterate through people and build a list of affiliations {% endcomment %}
{% assign affArray = "a, b, c" | split: ", " %}

{% for person in site.team %}

  {% if forloop.first == true %}
    {% assign affArray = person.affiliations %}
  {% else %}
    {% assign affArray = affArray | concat: person.affiliations %}
  {% endif %}
{% endfor %}
{% assign affArray = affArray | uniq %}

{% comment %} List each affiliation and the people in it {% endcomment %}

{% for affiliation in affArray %}
  <div class="card affiliation-list">
    <div class="card-header" data-toggle="collapse" data-target="#{{ affiliation }}">{{ affiliation }}</div>
    <div class="card-body collapse" id="{{ affiliation }}">
      {% for person in site.team %}
        {% if person.affiliations contains affiliation %}
          <button type="button" class="btn btn-block" onclick="window.location.assign('{{ '/' | relative_url }}people/#{{- person.firstname | append: person.lastname | replace: " ", "" -}}')">
            {{ person.firstname }} {{ person.lastname}}
          </button>
        {% endif %}
      {% endfor %}
    </div>
  </div>
{% endfor %}
