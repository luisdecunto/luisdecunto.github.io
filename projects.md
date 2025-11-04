---
layout: page
title: Projects
permalink: /projects/
---

A collection of my engineering and machine learning projects.

## Machine Learning

{%- assign ml_projects = site.projects | where: "category", "Machine Learning" | sort: "importance" %}
{%- for project in ml_projects %}
### [{{ project.title }}]({{ project.url | relative_url }})
{{ project.description }}
{%- endfor %}

## Computational Mechanics

{%- assign cm_projects = site.projects | where: "category", "Computational Mechanics" | sort: "importance" %}
{%- for project in cm_projects %}
### [{{ project.title }}]({{ project.url | relative_url }})
{{ project.description }}
{%- endfor %}
