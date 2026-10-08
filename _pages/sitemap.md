---
layout: single
title: "Sitemap"
permalink: /sitemap/
author_profile: true
---

## Pages

{% for item in site.data.navigation.main %}
- [{{ item.title }}]({{ item.url | relative_url }})
{% endfor %}

## Publications

{% assign papers = site.publications | sort: 'order' %}
{% for paper in papers %}
- [{{ paper.title }}]({{ paper.url | relative_url }}) ({{ paper.year }})
{% endfor %}

## Projects

{% assign projects = site.portfolio | sort: 'order' %}
{% for project in projects %}
- [{{ project.title }}]({{ project.url | relative_url }})
{% endfor %}
