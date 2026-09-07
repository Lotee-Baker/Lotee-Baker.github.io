
---
title: Portfolio
layout: single
permalink: /portfolio/
classes: wide
---

Welcome to my Portfolio

My experience spans animatronics, prototyping, structural design, mechatronics, and advanced manufacturing, with projects ranging from interactive entertainment systems to industrial automation and experimental devices.

This portfolio showcases how I apply engineering fundamentals, hands-on fabrication, and problem-solving to create solutions that are both practical and engaging.

## Design Engineering

{% assign design_projects = site.portfolio | where_exp: "project", "project.categories contains 'Design Engineering'" %}

<div class="grid__wrapper">
  {% for project in design_projects %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>

## Advanced Manufacturing

{% assign manufacturing_projects = site.portfolio | where_exp: "project", "project.categories contains 'Advanced Manufacturing'" %}

<div class="grid__wrapper">
  {% for project in manufacturing_projects %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>

## Mechatronics & Automation

{% assign mechatronics_projects = site.portfolio | where_exp: "project", "project.categories contains 'Mechatronics & Automation'" %}

<div class="grid__wrapper">
  {% for project in mechatronics_projects %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>

## Entertainment Engineering

{% assign entertainment_projects = site.portfolio | where_exp: "project", "project.categories contains 'Entertainment Engineering'" %}

<div class="grid__wrapper">
  {% for project in entertainment_projects %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>

## Research & Experimental

{% assign research_projects = site.portfolio | where_exp: "project", "project.categories contains 'Research & Experimental'" %}

<div class="grid__wrapper">
  {% for project in research_projects %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>

