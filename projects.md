---
layout: page
title: Projects
order: 2
---

<section id="projects">
{% assign projects = site.data.projects | where_exp: "proj", "proj.hidden == nil" %}
{% for proj in projects %}
    {% include project.html proj=proj %}
{% endfor %}
</section>