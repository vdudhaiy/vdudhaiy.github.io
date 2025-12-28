---
layout: page
title: Coursework
permalink: /coursework/
last_updated: 2025-12-28
--- 
<p style="text-align: right;">
  <small>Last Updated: {{ page.last_updated | date: "%b %-d, %Y" }}</small>
</p>

# Purdue University
#### Bachelor of Science in Computer Engineering

**Relevant Coursework:**
{% assign sorted_courses = site.coursework | sort: "sort_key" %}

<ul>
  {% for course in sorted_courses %}
    <li>
      <a href="{{ course.url | relative_url }}">{{ course.code }} : {{ course.title }}</a>
      <small>({{course.semester}} {{ course.year}})</small>
      <p>Grade Secured: {{course.grade}}</p>

    </li>
  {% endfor %}
</ul>

_Click on the course to learn more._