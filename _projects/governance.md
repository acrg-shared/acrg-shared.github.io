---
layout: page
title: platform governance
description: How should online platforms be governed to minimize harms to their users?
img: /assets/img/midjourney/governance.png.jpg
project: Governance
groups: [faculty, students]
importance: 1
---

<h2> what is platform governance? </h2>
  <p style="text-align: justify">
    Platform governance refers to the set of rules, policies, and practices that govern the behavior, content, and 
    interactions taking place on online platforms. It involves the establishment of guidelines and regulations by 
    platform operators to ensure the proper functioning, safety, and fairness of their platforms.

    Online platforms, such as social media platforms, search engines, e-commerce sites, and sharing economy platforms,
    have become powerful intermediaries that connect users, facilitate transactions, and enable the exchange of 
    information. Given their influential role and the potential for misuse or harm, platform governance has become 
    a crucial aspect of managing these digital spaces.
    <br><br>
    
    At the SPARTA lab, we're interested in developing policies and technological solutions to improve the governance
    of online social media platforms. Our current work is focused on understanding how online community moderation
    can be improved through technological and economic interventions.
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