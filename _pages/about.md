---
layout: about
title: about
permalink: /
subtitle: 

profile:
  align: left
  image: 
  image_circular: false # crops the image to make it circular
  address: >

news: true  # includes a list of news items
latest_posts: false  # includes a list of the newest posts
selected_papers: false # includes a list of papers marked as "selected={true}"
social: false  # includes social icons at the bottom of the page
---

---
#### about acrg
<p style="text-align: justify">
The Algorithms and Culture Research Group (ACRG) seeks to study and address the multifaceted impacts of technology on culture, exploring both its unintentional and harmful consequences, as well as its potential benefits. We view technology as a powerful force that profoundly influences the way individuals perceive and engage with the world. At the same time, we are interested in how individuals leverage technology to exercise agency and resistance, transforming it into a tool for empowerment and self-expression. </p>
<p style="text-align: justify">
Through our interdisciplinary approach, we strive to contribute to a better understanding of the intricate interplay between algorithms and culture, fostering critical discussions and paving the way for a more nuanced future.
</p>

---
#### history
<p style="text-align: justify">
ACRG was formed in 2015 as an interdisciplinary reading group based at the University of Iowa <a href="https://obermann.uiowa.edu/">Obermann Center for Advanced Studies</a>. The purpose of the reading group was to learn how scholars in various disciplines were talking about and studying algorithms. Over time, ACRG evolved into a research group committed to true interdisciplinarity, guided by the belief that our work is strengthened by incorporating insights, theories, and methodologies from a variety of academic paradigms. Today, the ACRG consists of members from universities across the United States interested in studying the relationship between algorithms and culture.
</p>

---
#### research projects

<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
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



---

#### acknowledgements

<p style="text-align: justify">
ACRG is supported by grants from the Department of Defense Minerva Research Initiative and managed through the Air Force Office of Scientific Research.
</p>

<p style="text-align: center">
<img src="assets/img/USDoD_seal.png" width="150px">
<img src="assets/img/afosr.png" width="150px">
</p>

---

