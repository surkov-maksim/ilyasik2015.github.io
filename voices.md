---
layout: default
title: Голосовые сообщения из Telegram
seo:
  type: person
---

{% assign audio_files = site.static_files | where: "audio", true %}
{: style="font-size:16px;font-weight:bold;"}{% for myaudio in audio_files %}
  1. <audio controls><source src="{{ myaudio.path }}" type="audio/ogg">Your browser does not support the audio tag. [Download {{ myaudio.basename }}]({{ myaudio.path }})</audio><br/>
{% endfor %}
