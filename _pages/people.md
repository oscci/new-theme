---
title: "People"
tagline: "Find your key contacts"
description: Key people involved in ReproducibleResearchOxford
permalink: /people/
type: page
---

<div class="initial-content person-card-columns" id="accordion">
  {% for person in site.team %}
    {% include person_card person=person %}
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


{% assign affArray = "a, b, c" | split: ", " %}
{% for person in site.team %}
  {% if forloop.first == true %}
    {% assign affArray = person.affiliations %}
  {% else %}
    {% assign affArray = affArray | concat: person.affiliations %}
  {% endif %}
{% endfor %}
{% assign affArray = affArray | uniq %}

{% for a in affArray %}
  {% include affiliation_list affiliation=a %}
{% endfor %}

<script>
  setTimeout(function () {
    openCard();
  }, 100);
</script>
