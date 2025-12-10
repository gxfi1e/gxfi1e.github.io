---
show: true
width: 4
height: 295px
date: 2021-09-12 00:01:00 +0800

images:
  - src: '{{ "assets/images/photos/KAUST.jpg" | relative_url }}'
    class: "img-fluid rounded-xl"
    title: "KAUST Storm"
    desc: "First place masterpiece"

  - src: '{{ "assets/images/photos/MATT.jpg" | relative_url }}'
    class: "img-fluid rounded-xl"
    title: "Matterhorn"
    desc: "Blue moment"

  - src: '{{ "assets/images/photos/DOLO.jpg" | relative_url }}'
    class: "img-fluid rounded-xl"
    title: "Sunset Dolomite"
    desc: "Dolomite"
---

{% include widgets/carousel.html id=page.id images=page.images height=page.height %}
