---
layout: page
title: auditing privacy
description: Bringing transparency and compliance verification to the online data ecosystem
img: /assets/img/midjourney/auditor.png.jpg
project: Privacy
groups: [faculty, students]
importance: 1
---


<h2> what is privacy auditing? </h2>
  <p style="text-align: justify">
        Privacy auditing refers to the process of evaluating and assessing an organization's practices, procedures, 
        and systems to ensure compliance with privacy laws, regulations, and industry standards. It involves a systematic 
        examination of an organization's privacy policies, data handling practices, security measures, and data protection 
        controls to identify any gaps, vulnerabilities, or areas of non-compliance related to privacy. The goal is to 
        ensure that personal data is collected, used, stored, and shared in a manner that respects individuals' privacy 
        rights and maintains the confidentiality, integrity, and availability of the data.
        <br><br>
        At the SPARTA lab, we're interested in developing methodologies and policy recommendations to enable to 
        automated detection of non-compliance with privacy regulations. The research challenge is to satisfy the 
        need for high-quality audits while being denied access to the internals of the systems that are the focus of 
        the audits.
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