---
layout: page
title: Projects
permalink: /projects/
--- 

{% assign sorted_projects = site.projects | sort: "start_date" | reverse %}
<ul>
  {% for project in sorted_projects %}
    <li>
      <a href="{{ project.url | relative_url }}">{{ project.title }}</a>
      <small>
        {% if project.start_date %}Start: {{ project.start_date | date: "%b %-d, %Y" }}{% endif %}
        {% if project.end_date %} — End: {{ project.end_date | date: "%b %-d, %Y" }}{% endif %}
      </small>
      <p>{{ project.summary }}</p>
    </li>
  {% endfor %}
</ul>