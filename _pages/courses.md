---
title: "D3C - Courses"
layout: textlay
excerpt: "D3C -- Courses"
sitemap: false
permalink: /courses/
tags: [10001, 10002]
---

# PhD courses 
{% assign number_printed = 0 %}
{% for theme-item in site.data.courses %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if theme-item.highlight == 1 %}

{% if even_odd == 0 %}

<div class="row">
{% endif %}
{% if theme-item.long == 1 %}
<div class="col-sm-12 clearfix">
 <div class="well">
 {% if theme-item.hasimage == 1 %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/courses/{{ theme-item.image }}" class="img-responsive" width="{{ theme-item.width }}" style="float: top"/>
  {% endif %}
  <h3><pubtit>{{ theme-item.title }}</pubtit></h3>
  <p>{{ theme-item.description }}</p>
{% if theme-item.haslink == 1 %}
  <a href="{{theme-item.link}}"  class="btn-bib" style="text-decoration:none; color:#ebebeb; hover:#ebebeb;" role="button" aria-expanded="false">Link to course page</a>
    {% endif %}
</div>
</div>
{% else %}
<div class="col-sm-6 clearfix">
 <div class="well">
 {% if theme-item.hasimage == 1 %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/courses/{{ theme-item.image }}" class="img-responsive" width="{{ theme-item.width }}" style="float: top"/>
  {% endif %}
  <h3><pubtit>{{ theme-item.title }}</pubtit></h3>
  {{ theme-item.description }}
<p><b>Teachers:</b> {{ theme-item.teachers }}</p>
<p><b>Given next time:</b> {{ theme-item.next }}</p>
{% if theme-item.haslink == 1 %}
<div>
  <a href="{{theme-item.link}}"  class="btn-bib" style="text-decoration:none; color:#ebebeb; hover:#ebebeb;" role="button" aria-expanded="false">Link to course page</a>
</div>
{% endif %}
 </div>
</div>
{% assign number_printed = number_printed | plus: 1 %}
{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}

</div>
{% endif %}

<p> &nbsp; </p>
