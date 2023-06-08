---
layout: page
title: network measurement
description: Developing tools and methodologies to help measure the Internet accurately.
img: /assets/img/midjourney/measurement.png.jpg
project: Measurement
groups: [faculty, students]
importance: 1
---


<h2> what is network measurement? </h2>
  <p style="text-align: justify">
        Internet/network measurement refers to the collection, analysis, and interpretation of data related to the 
        structure, behavior, and performance of the internet. It involves studying various aspects of the internet 
        ecosystem, including network infrastructure, traffic patterns, protocols, services, and user behavior.
        It provides valuable insights into the functioning of the internet, facilitates the identification of 
        performance bottlenecks and security vulnerabilities, and helps in improving the overall efficiency 
        and reliability of internet infrastructure and services.
        <br><br>
        At the SPARTA lab, we're interested in developing methodologies to perform high-quality measurements of a
        broad range of Internet ecosystems. Generally, we're interested in uncovering the security trade-offs posed
        by new networked technologies. Our current research is focused on uncovering the unintended security consequences
        of broad IPv6 and LEO Internet (e.g., Starlink) deployments.
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