---
layout: default
permalink: /blog/
title: Blog
nav: true
nav_order: 1
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

  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        <h3>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </h3>
        <p>{{ post.date | date: "%B %d, %Y" }}</p>
        {% if post.description %}
          <p>{{ post.description }}</p>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</div>
