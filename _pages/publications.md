---
layout: single
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
[Google Scholar]({{ site.author.googlescholar }})
{% endif %}

{% assign papers = site.publications | sort: "order" %}
{% assign current_year = '' %}
{% for paper in papers %}
{% if paper.year != current_year %}
{% assign current_year = paper.year %}

## {{ current_year }}

{% endif %}
{% include publication.html paper=paper %}
{% endfor %}
