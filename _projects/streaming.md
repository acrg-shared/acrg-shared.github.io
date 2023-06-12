---
layout: page
title: streaming video
description: What about a category for the type of things Ryan and Tim do on algorithms and streaming?
img: /assets/img/midjourney/measurement.png.jpg
project: Streaming
groups: [co-directors, faculty, students]
importance: 1
---


  <p style="text-align: justify">
Relevant text goes here
  </p>
<hr>

<h2> researchers </h2>
<div class="projects">
    <div class="grid">
        {%- for category in page.groups %}
            {%- assign people_groups = site.data.people | where: "category", category -%}
            {%- assign people_project = people_groups | where_exp: "item", "item.projects contains page.project" -%}
            {%- for person in people_project %}
                {%- include person.html %}
            {%- endfor %}
        {%- endfor %}
    </div>
</div>
<hr>

<h2> research output </h2>
  <p style="text-align: justify">
    Below is a list of publications from our research on this fourth unknown category.
  </p>
<div class="publications">
{%- for y in page.project %}
{% bibliography -f {{ site.scholar.bibliography }} -q @*[abbr={{y}}]* %}
{% endfor %}
</div>
<hr>
