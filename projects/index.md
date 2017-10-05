---
layout: default
title: Projects
order: 1
---

{% for projects in site.projects %}
## [{{ projects.title }}]({{ projects.url | prepend: site.baseurl }})
{{ projects.duration }}
{% endfor %}
