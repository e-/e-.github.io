---
layout: home
title: Home
---


<h2>Publications</h2>
{% assign sorted_publications = site.data.publications %}

{% for pub in sorted_publications %}
{% include publication.html pub = pub %} 
{% endfor %}
