---
layout: default
title: Home
---

<h1>📝 Latest Blog Posts</h1>

<div class="post-grid">
  {% for post in site.posts %}
    <div class="post-tile">
      {% if post.thumbnail %}
    <img src="{{ post.thumbnail }}" alt="Thumbnail for {{ post.title }}" class="post-thumb" />
  {% endif %}
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
      <p>{{ post.excerpt }}</p>
      <a class="read-more" href="{{ post.url }}">Read more →</a>
    </div>
  {% endfor %}
</div>
