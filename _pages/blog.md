---
layout: default
permalink: /blog/
title: blog
nav: true
nav_order: 1
pagination:
  enabled: false
---

<div class="post">
  {% if site.blog_name or site.blog_description %}
    <div class="header-bar">
      {% if site.blog_name %}
        <h1>{{ site.blog_name }}</h1>
      {% endif %}
      {% if site.blog_description %}
        <h2>{{ site.blog_description }}</h2>
      {% endif %}
    </div>
  {% endif %}
</div>
