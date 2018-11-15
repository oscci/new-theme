---

type: page
permalink: /main_test2
layout: splash
classes: landing

header:
  overlay_color: "#000"
  overlay_filter: "0.2"
  overlay_image: images/dukehumphreys.jpg
  actions:
#    - label: "Download"
      url: "https://github.com/mmistakes/minimal-mistakes/"
#  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"

intro:
  - excerpt: 'Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean
commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus
et magnis dis parturient montes, nascetur ridiculus mus. Donec quam
felis, ultricies nec, pellentesque eu, pretium quis, sem.'

feature_row:
  - image_path: assets/images/unsplash-gallery-image-1-th.jpg
    alt: "placeholder image 1"
    title: "About"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
  - image_path: /assets/images/unsplash-gallery-image-2-th.jpg
    image_caption: "Image courtesy of [Unsplash](https://unsplash.com/)"
    alt: "placeholder image 2"
    title: "Events"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
    url: "#test-link"
    btn_label: "Read More"
    btn_class: "btn--primary"
  - image_path: /assets/images/unsplash-gallery-image-3-th.jpg
    title: "Resources"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."

---

{% include feature_row id="intro" type="center" %}

Discover more [about](/new-theme/about/) what we do, check out our
[events](/new-theme/events) and [resources](/new-theme/resources)!