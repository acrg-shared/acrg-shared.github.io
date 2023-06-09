---
layout: page
permalink: /people/
title: team
nav: true
nav_order: 1
display_categories: [faculty, students, alumni]
---start_years: [2018, 2019, 2020, 2021, 2022, 2023, 2024]
---

<!-- pages/people.md -->

<div class="projects">
    {%- for category in page.display_categories %}
        {%- assign people_groups = site.data.people | where: "category", category -%}
        <h2 class="category"> {{ category }} </h2>
    {%- endfor %}
</div>
