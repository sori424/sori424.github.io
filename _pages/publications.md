---
layout: page
permalink: /publications/
title: Publications
description: publications by categories in reversed chronological order. 
years: [2021,2020]
nav: true
---

<div class="publications">

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

{% for y in page.html%}
  <h2 class="html">{{y}}</h2>
  {% bibliography -f papers -q @*[html={{y}}]* %}
{% endfor %}

</div>
