---
layout: page
title: online manipulation
description: How are opinions manipulated by people and algorithms online?
img: /assets/img/midjourney/manipulation.png.jpg
project: Manipulation
groups: [faculty, students]
importance: 1
---

<h2> what is online manipulation? </h2>
  <p style="text-align: justify">
        Online manipulation refers to the act of deliberately influencing 
        or controlling the thoughts, opinions, behaviors, or actions of individuals 
        or groups through online platforms and digital communication channels. It 
        involves the use of a broad variety of techniques, strategies, and tactics to exploit 
        vulnerabilities and manipulate people's emotions, beliefs, and decisions. 
        Online manipulation is often employed for purposes such as political 
        propaganda, advertising, social engineering, or spreading misinformation.
        <br><br>
        At the SPARTA lab, we're interested in developing a stronger understanding of the processes by which
        Internet users are manipulated by other users and by platform algorithms (e.g., recommendation systems). 
        Our ultimate goal is to develop technological and policy interventions that are able to protect consumers
        from manipulation online.
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
    Peruse the following publications from our lab to learn about our related research and findings.
  </p>
<div class="publications">
{%- for y in page.project %}
{% bibliography -f {{ site.scholar.bibliography }} -q @*[abbr={{y}}]* %}
{% endfor %}
</div>
<hr>