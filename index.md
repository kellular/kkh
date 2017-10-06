---
layout: default
title: Projects
order: 1
---

{% for projects in site.projects %}
  <ul class="c-pane">
    <li>
      <a class="" href="{{ site.baseurl }}{{ projects.url }}">
        <img src="{{ site.baseurl }}/images/{{ projects.thumbnail }}.png" alt="">
        <h2>{{ projects.title }}</h2>
      </a>
    </li>
  </ul>
{% endfor %}
