---
layout: default
title: Видео из Telegram
seo:
  type: person
---

{% assign video_files = site.static_files | where: "video", true %}
{: style="font-weight:bold;"}{% for myvideo in video_files %}
  <video controls><source src="{{ myvideo.path }}" type="video/mp4">Your browser does not support the video tag. [Download {{ myvideo.basename }}]({{ myvideo.path }})</video><br/>
{% endfor %}
