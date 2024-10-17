---
layout: page
title: Blog
subtitle: Select ramblings of Pudhina
---

<div>
  <ul class="list-posts">
    {% for post in site.posts %}
    <li class="post-teaser" style="margin-bottom: 30px;">
      <!-- Post title -->
      <h2 class="post-teaser__title">{{ post.title }}</h2>
      <!-- Post-specific image wrapped in a link -->
      <a href="{{ post.url | prepend: site.baseurl }}">
        <img src="{{ post.image | prepend: site.baseurl }}" id="post-img" style="width: 100%; height: auto;">
      </a>
    </li>
    {% endfor %}
  </ul>
</div>
