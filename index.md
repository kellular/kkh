---
layout: default
title: Projects
order: 1
---

{% for projects in site.projects %}
  <ul class="c-pane" style="margin-bottom: 3rem;">
    <li>
      <a class="" style="text-decoration: none;" href="{{ site.baseurl }}{{ projects.url }}">
        <img src="{{ site.baseurl }}/images/{{ projects.thumbnail }}.png" alt="">
        <h4 style="margin-top: 0.5rem; margin-bottom: 0rem;">{{ projects.title }}</h4>
        <h6 style="margin-top: 0rem;">{{ projects.duration }}</h6>
      </a>
    </li>
  </ul>
{% endfor %}
