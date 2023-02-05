---
layout: page
permalink: /features/
title: Features
description: The following is a showcase of the features of the web-app.
years: [2023, 2022]
nav: true
nav_order: 1
---

<!-- _pages/publications.md -->
<div class="publications">

<div class="card mt-3 wow fadeIn" data-wow-delay="1s" style="padding: 1rem;">
  In addition to this page, sheet music can also be found under "Resources".
</div>

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
