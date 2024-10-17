---
layout: page
title: Blog
subtitle: Select ramblings of Pudhina
---

<div>
  <ul class="list-posts" style="list-style-type: none; padding: 0;">
    {% for post in site.posts %}
    <li class="post-teaser" style="position: relative; margin-bottom: 30px; max-width: 600px;">
      <!-- Image container with relative positioning -->
      <a href="{{ post.url | prepend: site.baseurl }}" style="display: block; position: relative; text-decoration: none;">
        <img src="{{ site.baseurl }}/assets/img/{{ post.image }}" alt="Post Image" style="width: 100%; height: auto; display: block; max-height: 400px;">
        <!-- Title and subtitle overlay -->
        <div style="position: absolute; bottom: 10px; left: 10px; background: rgba(0, 0, 0, 0.5); color: white; padding: 10px; width: calc(100% - 20px); box-sizing: border-box;">
          <h2 class="post-teaser__title" style="margin: 0; font-size: 1.5em;">{{ post.title }}</h2>
          <h3 class="post-teaser__subtitle" style="margin: 0; font-size: 1.2em;">{{ post.subtitle }}</h3>
        </div>
      </a>
    </li>
    {% endfor %}
  </ul>
</div>
