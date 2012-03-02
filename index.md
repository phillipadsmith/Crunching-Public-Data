---
layout: page
title: Welcome to Crunching Public Data
tagline: Telling stories with big data
---
{% include JB/setup %}

<h4>Course updates:</h4>
<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
