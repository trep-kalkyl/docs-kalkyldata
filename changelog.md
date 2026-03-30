---
layout: default
title: Changelog
nav_order: 5
---

# Uppdateringar och Changelog
Här kan du se allt nytt som händer i systemet.

---

{% assign sorted_changelog = site.data.changelog | sort | reverse %}

{% for entry in sorted_changelog %}
  {% assign data = entry[1] %}
### {{ data.date }} – {{ data.title }}
{{ data.description }}

---
{% endfor %}
