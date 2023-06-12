---
layout: page
permalink: /people/
title: team
nav: true
nav_order: 1
display_categories: [co-directors, faculty, students]
---

<p style="text-align: center">
<img src="acrg_2023retreat.jpg" width="100%">
</p>

---

<!-- pages/people.md -->

<div class="projects">
    {%- for category in page.display_categories %}
        {%- assign people_groups = site.data.people | where: "category", category -%}
        <h2 class="category"> {{ category }} </h2>
            <div class="grid">
                {%- for person in people_groups %}
                    {%- include person.html %}
                {%- endfor %}
            </div>
    {%- endfor %}
</div>
