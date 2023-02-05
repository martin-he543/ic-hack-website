---
layout: page
title: Testimonials
permalink: /testimonials/
description: Some testimonials from some satisfied customers.
nav: true
nav_order: 2
display_categories: [Party Planning, Birthday Parties, Afternoon Tea, PTA Meeting, Lunch Meeting, Teenage Raucous Houseparty, Game Night, Rager Binge]
horizontal: false
---
<b>
  <a href="#Party Planning">Party Planning</a>&nbsp; &middot; &nbsp;<a href="#Birthday Parties">Birthday Parties</a>&nbsp; &middot; &nbsp;<a href="#Gatherings">Gatherings</a>&nbsp; &middot; &nbsp;<a href="#Afternoon Tea">Afternoon Tea</a>&nbsp; &middot; &nbsp;<a href="#Lunch Meeting">Lunch Meeting</a>&nbsp; &middot; &nbsp;<a href="#Teenage Raucous Houseparty">Teenage Raucous Houseparty</a>&nbsp; &middot; &nbsp;<a href="#Game Night">Game Night</a>&nbsp; &middot; &nbsp;<a href="#Rager Binge">Rager Binge</a>
</b>
<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category" id="{{ category }}">{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>
