---
layout: page
title: Experiences
permalink: /experiences/
--- 

{% assign sorted_xp = site.experiences | sort: "start_date" | reverse %}
<ul>
  {% for xp in sorted_xp %}
    <li>
      <a href="{{ xp.url | relative_url }}">{{ xp.role }}</a>
      <small>
        {% if xp.start_date %}Start: {{ xp.start_date | date: "%b %-d, %Y" }}{% endif %}
        {% if xp.end_date %}
        — End: {{ xp.end_date | date: "%b %-d, %Y" }}
        {% else %}
        — Present
        {% endif %}
      </small>
      <p><b>Company:</b> {{ xp.employer }}</p>
      <p><b>Location:</b> {{ xp.location }}</p>
      <p><b>Summary:</b> {{ xp.summary }}</p>
    </li>
  {% endfor %}
</ul>