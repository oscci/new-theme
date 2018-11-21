---
title: "RR OX"
type: page
permalink: /main_test3
layout: splash
classes: landing

header:
  overlay_color: "#000"
  overlay_filter: "0.4"
  overlay_image: images/dukehumphreys.jpg
excerpt: "Promoting robust research practices at Oxford University"

row1:
  - image_path: /images/dukehumphreys.jpg
    alt: "About RROxford"
    url: /about/    
    btn_label: "Find out more about us"
    btn_class: "btn--primary"
    title: "About"
    excerpt: 'We are a group of researchers at Oxford University, determined to
    stimulate reproducible and open research practices. Find out more about who
    we are, and discover who is involved in research reproducibility at your own
    department!'

row2:
  - image_path: /images/dukehumphreys.jpg
    url: /events/
    alt: "test photo"
    btn_label: "Upcoming events"
    btn_class: "btn--primary"
    title: "Our events"
    excerpt: 'We frequently organise events to promote robust research practices
    at Oxford University. During term time, there are weekly ReproducibiliTea
    journal clubs on Fridays, and an Open Science lecture on Wednesdays. Past
    events include hosting software and data carpentry workshops, in cooperation
    with Data Carpentry.'

row3:
  - image_path: /images/dukehumphreys.jpg
    alt: "test photo"
    btn_label: "Our resources"
    btn_class: "btn--primary"
    url: /resources/
    title: "Resources"
    excerpt: 'Interested in research reproducibility, but not sure where to
    start? We offer lots of online resources, including instructions on how to
    use GitHub.'

---

{% include feature_row id="row1" type="right" %}

{% include feature_row id="row2" type="left" %}

{% include feature_row id="row3" type="right" %}
