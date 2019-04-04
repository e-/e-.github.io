---
layout: post
title: Publications
order: 1
---
{% assign publications = site.data.publications | sort: "year" | reverse %}
{% assign international_publications = publications | where_exp: "item", "item.attrs contains 'international'" %}

{% assign domestic_publications = publications | where_exp: "item", "item.attrs contains 'domestic'" %}


<h2>International</h2>

{% for pub in international_publications %}
{% include publication.html pub = pub %} 
{% endfor %}

<h2>Domestic</h2>


{% for pub in domestic_publications %}
{% include publication.html pub = pub %} 
{% endfor %}