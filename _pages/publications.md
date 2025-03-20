---
layout: page
permalink: /publications/
title: Publications
description: My list of publications in peer-reviewed conferences.
years: [2025, 2024, 2023, 2022, 2020]
nav: true
---

<div class="publications">

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
