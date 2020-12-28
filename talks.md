---
layout: default
title: Talks
---
# Talks

{% assign talks_by_year = site.data.talks | group_by_exp: "talk", "talk.year" %}
{% for year in talks_by_year %}
## {{ year.name }}
  {% for talk in year.items %}
  - {{talk.title}} - {{ talk.conference }} ([slides]({{ talk.slides }}))
  {% endfor %}
{% endfor %}
