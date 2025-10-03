---
layout: default
title: Blog
permalink: /blog/
---

<div class="blog-list">
  {% for post in site.posts %}
    <div class="post-summary fade-in-section">
      {% if post.image %}
        <img src="{{ post.image }}" alt="{{ post.title }}">
      {% endif %}
      <div class="post-info">
        <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
        {% if post.description %}
          <p>{{ post.description | truncate: 120 }}</p>
        {% endif %}
        <p class="post-date"><small>{{ post.date | date: "%b %d, %Y" }}</small></p>
      </div>
    </div>
  {% endfor %}
</div>

