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
<p style="text-align: justify">
A little info about the Algorithms and Culture Research Group (ACRG).
</p>

---
#### history
<p style="text-align: justify; color: red">
ACRG was formed in 2015 as an interdisciplinary reading group based at the University of Iowa Obermann Center for Advanced Studies. The purpose of the reading group was to learn how scholars in various disciplines were talking about and studying algorithms. Over time, ACRG evolved into a research group committed to true interdisciplinarity, guided by the belief that our work is strengthened by incorporating insights, theories, and methodologies from a variety of academic paradigms. Today, the ACRG consists of members from universities across the United States interested in studying the relationship between algorithms and culture.
</p>

---
#### ongoing research

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
The SPARTA lab is supported by grants from the National Science Foundation, 
the Department of Defense, the Air Force Research Laboratory, Google Research,
and the University of Iowa.
</p>

<p style="text-align: center">
<img src="assets/img/NSF.png" width="150px">
<img src="assets/img/USDoD_seal.png" width="150px">
<img src="assets/img/afrl.png" width="150px">
<img src="assets/img/google_research.png" width="150px">
<img src="assets/img/uiowa_seal.png" width="150px">
</p>

<p style="text-align: justify">
Our research would not be possible without the support of our sponsors, 
the <a href="http://cs.uiowa.edu"> Department of Computer Science</a>, 
and the <a href="https://clas.uiowa.edu/linux/">CLAS Linux Group</a>.
</p>

---

