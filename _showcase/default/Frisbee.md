---
show: true
width: 4
date: 2020-01-12 00:01:00 +0800
---

<div>
  <!-- Background Image (outside overlay, same as reference code) -->
  <img data-src="{{ 'assets/images/etc/frisbee.png' | relative_url }}" 
       class="lazy w-100 rounded-xl"
       src="{{ '/assets/images/empty_300x200.png' | relative_url }}">

  <!-- Floating text box -->
  <div class="card-img-overlay" 
       style="overflow: visible; background: rgba(255,255,255,0.85); border-radius: 0.75rem; padding: 1rem;">
    <h5 class="card-title">Happy Frisbee</h5>
    <p class="card-text">
      Flying disc is a perfect blend of aerodynamics, coordination, and athletic spirit.
    </p>
  </div>
</div>
