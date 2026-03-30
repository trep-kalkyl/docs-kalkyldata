---
layout: default
title: Changelog
nav_order: 5
---

# Uppdateringar och Changelog
Här kan du se allt nytt som händer i systemet, från stort till smått.

---

{% assign changelog_array = site.data.changelog | sort %}

{% for entry in changelog_array reversed %}
  {% assign data = entry[1] %}
### {{ data.date }} – {{ data.title }}
{{ data.description }}

---
{% endfor %}
