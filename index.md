---
layout: default
title: Main page
weight: -10
---
## Welcome

{% assign pagelist = site.pages | sort_natural: 'weight' %}
{% for p in pagelist %}
  {% if p.title != nil %}
    {% if p.url == page.url %}
  - [{{ p.title }}]({{ p.url }})
    {% else %}
  - [{{ p.title }}]({{ p.url }})
    {% endif %}
  {% endif %}
{% endfor %}
