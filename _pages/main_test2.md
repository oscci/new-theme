---

type: page
permalink: /main_test2
layout: splash
classes: landing

header:
  overlay_color: "#000"
  overlay_filter: "0.2"
  overlay_image: images/dukehumphreys.jpg
#  actions:
#    - label: "Download"
#      url: "https://github.com/mmistakes/minimal-mistakes/"
#  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"

intro:
  - excerpt: 'Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean
commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus
et magnis dis parturient montes, nascetur ridiculus mus. Donec quam
felis, ultricies nec, pellentesque eu, pretium quis, sem.'

row1:
  - image_path: /images/dukehumphreys.jpg
    alt: "placeholder image 1"
    title: "About"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
  - image_path: /images/dukehumphreys.jpg
    image_caption: "Image courtesy of [Unsplash](https://unsplash.com/)"
    alt: "placeholder image 2"
    title: "Events"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
    url: "#test-link"
    btn_label: "Read More"
    btn_class: "btn--primary"
  - image_path: /images/dukehumphreys.jpg
    title: "Resources"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."

row2:
  - image_path: /images/dukehumphreys.jpg
    alt: "test photo"
    btn_label: "test photo"
    title: "yup i'm a test photo"
    excerpt: 'This is some sample content that goes here with **Markdown** formatting. Right aligned with `type="right"`'


---

{% include feature_row id="intro" type="center" %}

{% include feature_row id="row1" %}

{% include feature_row id="row2" type="right" %}

Discover more [about](/new-theme/about/) what we do, check out our
[events](/new-theme/events).

You can also check our [resources](/new-theme/resources)!
