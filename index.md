---
layout: page
title: Kata's for Software Developments
tagline: Because, sometimes talking about creating good software isn't enough...
---
{% include JB/setup %}

## Recent posts

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
