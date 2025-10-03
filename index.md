---
layout: default
title: Welcome to My Cloud Journey
---

<div class="landing-intro fade-in-section">
  <h1>Welcome to My Cloud & Security Journey!</h1>
  <p>Hi, I’m Happy. I’m a Junior Cloud Security Engineer, learning the ropes, making mistakes, and sharing everything I discover along the way. This site is my space to document my journey, experiments, and lessons in AWS and cloud security.</p>

  <img src="{{ '/assets/images/aws-journey.jpg' | relative_url }}" alt="Cloud Security Journey" class="landing-photo">
</div>

<div class="fade-in-section">
  <h2>Latest Posts</h2>
  {% for post in site.posts limit:3 %}
  <div class="post-summary fade-in-section">
    <img src="{{ post.image | default: '/assets/images/profile.jpg' }}" alt="{{ post.title }}">
    <div class="post-info">
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <p>{{ post.description | truncate: 120 }}</p>
    </div>
  </div>
  {% endfor %}
</div>
