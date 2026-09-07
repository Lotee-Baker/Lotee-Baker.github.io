---
title: Portfolio
layout: single
permalink: /portfolio/
classes: wide
---

Welcome to my Portfolio

My experience spans animatronics, prototyping, structural design, mechatronics, automation, and advanced manufacturing. My projects range from interactive show systems and industrial automation to experimental devices and hands-on mechanical design.

This portfolio showcases how I apply engineering fundamentals, hands-on fabrication, and problem-solving to create solutions that are both practical and engaging.

<div style="clear: both;"></div>

<h2>Design Engineering</h2>

{% assign design_projects = site.portfolio | where_exp: "project", "project.categories contains 'Design Engineering'" %}

<div class="grid__wrapper">
{% for project in design_projects %}
  {% assign post = project %}
  {% include archive-single.html type="grid" %}
{% endfor %}
</div>

<div style="clear: both;"></div>

<h2>Advanced Manufacturing</h2>

{% assign manufacturing_projects = site.portfolio | where_exp: "project", "project.categories contains 'Advanced Manufacturing'" %}

<div class="grid__wrapper">
{% for project in manufacturing_projects %}
  {% assign post = project %}
  {% include archive-single.html type="grid" %}
{% endfor %}
</div>

<div style="clear: both;"></div>

<h2>Mechatronics &amp; Automation</h2>

{% assign mechatronics_projects = site.portfolio | where_exp: "project", "project.categories contains 'Mechatronics & Automation'" %}

<div class="grid__wrapper">
{% for project in mechatronics_projects %}
  {% assign post = project %}
  {% include archive-single.html type="grid" %}
{% endfor %}
</div>

<div style="clear: both;"></div>

<h2>Research and Experimental</h2>

{% assign research_projects = site.portfolio | where_exp: "project", "project.categories contains 'Research and Experimental'" %}

<div class="grid__wrapper">
{% for project in research_projects %}
  {% assign post = project %}
  {% include archive-single.html type="grid" %}
{% endfor %}
</div>

<div style="clear: both;"></div>

<h2>Show Systems</h2>

{% assign show_projects = site.portfolio | where_exp: "project", "project.categories contains 'Show Systems'" %}

<div class="grid__wrapper">
{% for project in show_projects %}
  {% assign post = project %}
  {% include archive-single.html type="grid" %}
{% endfor %}
</div>

<div style="clear: both;"></div>

<h2>Misc</h2>

{% assign misc_projects = site.portfolio | where_exp: "project", "project.categories contains 'Misc'" %}

<div class="grid__wrapper">
{% for project in misc_projects %}
  {% assign post = project %}
  {% include archive-single.html type="grid" %}
{% endfor %}
</div>

<div style="clear: both;"></div>


