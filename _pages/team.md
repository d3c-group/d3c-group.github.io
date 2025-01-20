---
title: "D3C - Team"
layout: gridlay
excerpt: "D3C: Team members"
sitemap: false
permalink: /team/
---

# Group Members

This site is under construction.

## Current
{% for member in site.data.team_members %}

<div class="row">

<div class="col-sm-12 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/team/{{ member.photo }}" class="img-responsive" width="15%" style="float: left" />
  
  <div style='margin-left:20%;'>
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} <!--<br>email: <{{ member.email }}></i> -->
  
  <p style="font-size:.8em">{{ member.short_bio }}</p>
  </div>

  <p style="clear:both;"></p>
  <button class="button black" onclick="window.location.href='{{ member.website }}'" type="button">
  {{ member.name }}'s Personal Website</button>

</div>

</div>


{% endfor %}


## Alumni

{% assign number_printed = 0 %}
{% for member in site.data.alumni_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/team/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.duration }} <br> Role: {{ member.position }}</i> 
  <ul style="overflow: hidden">

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


