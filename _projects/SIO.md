---
layout: page
title: strategic information operations
description: How are user- and platform-specific vulnerabilities exploited by foreign actors?
img: /assets/img/midjourney/auditor.png.jpg
project: SIO
groups: [faculty, students]
importance: 1
---

  <p style="text-align: justify">
The United States and its allies are facing a growing threat of strategic information operations (SIO), influence campaigns organized by foreign actors to spread propaganda, disinformation, or manipulative content on social media platforms. Prior work has uncovered many dynamics of SIOs; however, what is lacking is an understanding of how user- and platform-specific vulnerabilities are exploited by SIOs to increase their reach and effectiveness. After all, SIOs do not merely take place on platforms, they are mediated through platforms. Platforms circulate content, including influence campaigns, through an algorithmic process that uses engagement metrics to map user preferences and classify posts. Platform algorithms, in turn, use this data to identify and deliver content deemed relevant to users, creating a feedback loop between user engagement and algorithmic curation. Within the context of SIOs, this means that how a user chooses to engage with propaganda, disinformation, or manipulative content will affect the likelihood that the platform delivers similar content to that user in the future. 
        <br><br>
We seek to taxonomize platforms’ vulnerabilities to SIOs while accounting for the dynamics between variables in the user-platform interaction model. After constructing this taxonomy, our secondary objective is to propose feasible mitigation strategies for the identified vulnerabilities. Further, our research examines user engagement in three regional contexts—the United States, Central & Eastern Europe, and East Africa—to understand vulnerabilities to SIOs in the U.S. as well as key allies that have been targeted by Russian and Chinese SIOs. 
        <br><br>
Our research design is innovative, in part, because it deeply integrates humanistic, social scientific, and computational methods to develop a holistic understanding of platforms’ vulnerabilities to SIOs. In addition, our study is grounded in mixed methods exploratory-explanatory sequential design so that each aim informs the research design of the aim that follows it. 
        <br><br>
  This research is funded by a 3-year grant from the <a href="https://www.defense.gov/News/Releases/Release/Article/3408680/dod-awards-18-million-for-academic-research-on-the-socio-political-drivers-of-f/">Minerva Research Initiative</a> (2023-2026).

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
    Below is a list of publications from our research on strategic information operations.
  </p>
<div class="publications">
{%- for y in page.project %}
{% bibliography -f {{ site.scholar.bibliography }} -q @*[abbr={{y}}]* %}
{% endfor %}
</div>
<hr>
