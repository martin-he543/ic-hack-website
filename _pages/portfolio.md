---
layout: page
permalink: /portfolio/
title: portfolio
description: The following is a showcase of various things I have composed and arranged over the years, to varying degrees of quality.
years: [2022, 2020, 2019, 2018, 2017, 2016, 2015, 2014]
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
