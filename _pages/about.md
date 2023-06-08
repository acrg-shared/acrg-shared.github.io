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
The <b>Sentinels for Privacy-Aware and Responsible Technological Advancement (SPARTA)</b> 
lab is a team of researchers at the <b> University of Iowa </b> who enjoy working towards 
improving privacy, accountability, and safety of Internet-connected emerging technologies 
and platforms. 

Beyond technical research and solutions, the team is also interested in achieving a 
better understanding of the underlying economic, social, legal, and ethical issues that 
make online privacy, accountability, and safety difficult to achieve.
</p>

---
#### join us!
<p style="text-align: justify; color: red">
The SPARTA lab is always interested in recruiting talented and self-motivated 
undergraduates (already at the University of Iowa) and Ph.D. students who want 
to improve the privacy and safety of emerging technologies. 
If that's you, please read the 
<a href="http://sparta.cs.uiowa.edu/manifesto">lab manifesto</a> and get in touch
with <a href="https://sparta.cs.uiowa.edu/people/rishab">Prof. Rishab Nithyanand</a> 
to discuss research opportunities available within the lab.
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

