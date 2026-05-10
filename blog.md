---
layout: page
title: Blog
permalink: /blog/
---

<div class="col-lg-12 text-center">
  <h2 class="section-heading text-uppercase">Blog</h2>
  <h3 class="section-subheading text-muted">Thoughts on storytelling, editing, creative process, and digital craft.</h3>
</div>

{% if site.posts.size > 0 %}
<ul class="list-unstyled">
  {% for post in site.posts %}
    <li class="mb-5">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p class="text-muted">{{ post.date | date: "%B %-d, %Y" }}</p>
      {% if post.excerpt %}
        <p>{{ post.excerpt | strip_html | truncatewords: 35 }}</p>
      {% endif %}
    </li>
  {% endfor %}
</ul>
{% else %}
<p class="text-center">No posts yet. New reflections are coming soon.</p>
{% endif %}
