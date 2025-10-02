---
layout: default
title: Blog
permalink: /blog/
---

# My Story
{% for post in site.posts %}
  <div class="post-summary fade-in-section">
    <img src="{{ post.image | default: '/assets/images/default-post.jpg' }}" alt="{{ post.title }}">
      <div class="post-info">
        <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
        <p>{{ post.description | truncate: 120 }}</p>
        <p class="post-date">{{ post.date | date: "%b %d, %Y" }}</p>
      </div>
  </div>
{% endfor %}
