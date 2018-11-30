---
title: "Posts by Category"
permalink: /categories/
layout: categories
author_profile: false
---


{% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% for post in category[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}


{% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% for page in category[1] %}
      <li><a href="{{ page.url }}">{{ page.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

{% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% for pages in category[1] %}
      <li><a href="{{ pages.url }}">{{ pages.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}


{% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% for pages in category[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

{% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% for pages in category[1] %}
      <li><a href="{{ page.url }}">{{ page.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
