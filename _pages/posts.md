---
layout: archive
title: "Blog"
permalink: /blog/
author_profile: true
---

My NHH has a summary of a lot of my [dissimination work](https://www.nhh.no/en/employees/faculty/carsten-gero-bienz/#tab5), mostly in Norwegian.

{% include base_path %}

{% capture written_year %}'None'{% endcapture %}

{% for post in site.posts %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  {% if year != written_year %}
  ## {{ year }}
  {% capture written_year %}{{ year }}{% endcapture %}
  {% endif %}
  {% include archive-single.html %}
{% endfor %}
