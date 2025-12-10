---
show: true
width: 4
height: 295px
date: 2021-09-12 00:01:00 +0800

images:
  - src: "{{ 'assets/images/photos/KAUST.jpeg' | relative_url }}"
    class: "img-fluid rounded-xl"
    title: "Photo 1"
    desc: "Description 1."

  - src: "{{ 'assets/images/photos/MATT.jpeg' | relative_url }}"
    class: "img-fluid rounded-xl"
    title: "Photo 2"
    desc: "Description 2"

  - src: "{{ 'assets/images/photos/DOLO.jpeg' | relative_url }}"
    class: "img-fluid rounded-xl"
    title: "Photo 3"
    desc: "Description 3"
---

{% include widgets/carousel.html id=page.id images=page.images height=page.height %}
