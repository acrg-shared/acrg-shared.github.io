---
layout: page
title: radicalization
description: What is the relationship between algorithmic personalization and online radicalization?
img: /assets/img/midjourney/governance.png.jpg
project: Radicalization
groups: [faculty, students]
importance: 1
---

  <p style="text-align: justify">
  
From YouTube functioning as “the great radicalizer” (Tufekci, 2018) to the spread of misinformation on Facebook and Twitter (Allcott, Gentzkow, & Yu, 2019), social media algorithms that personalize user content pose a significant concern for American national security. What users click, like, share, read, watch, and comment on is used by social media platforms as input for their proprietary algorithms that determine future content users see. With those inputs, algorithmic personalization can intensify “reinforcing spirals” (Slater, 2007) in which a user’s media choices affect their interests which, in turn, affect their future media choices and so on, producing a negative feedback loop that can lead toward extremism. Studying the interplay between the technological features of personalization algorithms and the psychological attributes and interpretive strategies of users can help us understand how individuals become radicalized online. Therefore, it is vitally important to identify technological, psychological, and cultural factors that lead to the radicalization of vulnerable populations on social media through the algorithmic personalization of content. 
    <br><br>
We define radicalization broadly to capture not only forms of violent religious extremism but also the adoption of extreme political, social, and cultural beliefs that deviate greatly from moderate or “mainstream” views. Our conceptualization is consistent with previous scholarship that defines radicalization as a relative concept consisting of a set of diverse processes (Borum, 2011; Sedgwick, 2010). Similarly, we define extremist content as that which differs significantly from someone’s current/previous views or from perceived “mainstream” views on an issue. Using these definitions, we believe users can view extreme content or be radicalized on a number of different issues and topics. Our previous work (Le et al., 2019) has shown that algorithmic personalization is higher for populations with extreme ideological beliefs, and there is mounting anecdotal evidence that individuals who feel disenfranchised are particularly vulnerable to becoming radicalized by extremist content on social media (Mak, 2018; Roose, 2019; Turkewitz & Roose, 2018). Therefore, there is an urgent need to identify factors that make one vulnerable to online radicalization and to develop and validate methodologies that can predict the likelihood of becoming radicalized online. 
    <br><br>
Our research design is innovative, in part, because it offers a mixed methods approach to studying the relationship between algorithmic personalization and online radicalization. Our research team employs qualitative, quantitative, and computational methodologies in the form of a longitudinal survey, behavioral data tracking, in-depth interviews, and sock-puppet auditing to discover the factors that lead to radicalization. 
      <br><br>
This research is funded by a 3-year grant from the <a href="https://minerva.defense.gov/Research/Funded-Projects/Article/2463751/algorithmic-personalization-and-online-radicalization/">Minerva Research Initiative</a>.
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
    Below is a list of publications from our research on radicalization.
  </p>
<div class="publications">
{%- for y in page.project %}
{% bibliography -f {{ site.scholar.bibliography }} -q @*[abbr={{y}}]* %}
{% endfor %}
</div>
<hr>
