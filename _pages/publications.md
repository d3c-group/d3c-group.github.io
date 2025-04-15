---
title: "D3C - Publications"
layout: gridlay
excerpt: "D3C -- Publications."
sitemap: false
years: [2024, 2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012]
permalink: /publications/
---
<!-- _pages/publications.md -->

# Publications

(See also the personal webpage of our group members)


## List of Publications

<div class="publications">

{%- for y in page.years %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f d3c_publications -q @*[year={{y}}]* %}
{% endfor %}

</div>
