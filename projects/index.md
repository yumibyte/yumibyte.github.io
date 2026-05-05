---
layout: page
title: Projects
permalink: /projects/
---

# Projects

<ul class="project-index">
{% for p in site.data.projects %}
  <li>
    <h2><a href="{{ site.baseurl }}/projects/{{ p.slug }}/">{{ p.title }}</a></h2>
    <p>{{ p.summary }}</p>
  </li>
{% endfor %}
</ul>
