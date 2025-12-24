---
layout: page
title: Coursework
permalink: /coursework/
--- 
# Purdue University
#### Bachelor of Science in Computer Engineering
{% assign semester_map = "Spring:1,Fall:2,Summer:3" | split: "," %}
{% assign sorted_courses = site.coursework | sort: "semester_order" | sort: "year" | reverse %}

<ul>
  {% for course in site.coursework %}
    <li>
      <a href="{{ courses.url | relative_url }}">{{ course.code }} : {{ course.title }}</a>
      <small>({{course.semester}} {{ course.year}})</small>
      <p>{{course.summary}}</p>

    </li>
  {% endfor %}
</ul>