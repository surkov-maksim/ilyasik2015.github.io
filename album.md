---
layout: default
title: Фотографии
seo:
  type: person
---

{% assign image_files = site.static_files | where: "image", true %}
{:style="list-style-type: none;"}{% for myimage in image_files %}
{% if myimage.path contains 'logo.png' %}{% continue %}{% endif %}
  - ![Балакин Илья Владимирович]({{ myimage.path }})
{% endfor %}
