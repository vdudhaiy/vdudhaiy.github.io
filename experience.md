---
layout: page
title: Experience
permalink: /experience/
--- 
Here's a list of my relevant work experience. Click on the experience to learn more. 

{% assign sorted_xp = site.experience | sort: "start_date" | reverse %}
<ul>
  {% for xp in sorted_xp %}
    <li>
      <a href="{{ xp.url | relative_url }}">{{ xp.role }}</a>
      <small>
        {% if xp.start_date %} {{ xp.start_date | date: "%b %-d, %Y" }}{% endif %}
        {% if xp.end_date %}
        — {{ xp.end_date | date: "%b %-d, %Y" }}
        {% else %}
        — Present
        {% endif %}
      </small>
      <p><b>Company/Institution:</b> {{ xp.employer }}</p>
      <p><b>Location:</b> {{ xp.location }}</p>
      <p><b>Summary:</b> {{ xp.summary }}</p>
    </li>
  {% endfor %}
</ul>