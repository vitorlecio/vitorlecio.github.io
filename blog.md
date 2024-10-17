---
layout: page
title: Blog
subtitle: Select ramblings of Pudhina
---

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px;">
  <ul class="list-posts" style="list-style-type: none; padding: 0;">
    {% for post in site.posts %}
    <li class="post-teaser" style="position: relative; margin-bottom: 30px;">
      <!-- Image container with relative positioning -->
      <a href="{{ post.url | prepend: site.baseurl }}" style="display: block; position: relative; text-decoration: none;">
        <img src="{{ site.baseurl }}/assets/img/{{ post.image }}" alt="Post Image" style="width: 100%; height: auto; display: block; max-height: 400px;">
        <!-- Title and subtitle overlay -->
        <div style="position: absolute; bottom: 10px; left: 10px; background: rgba(0, 0, 0, 0.6); color: white; padding: 15px; width: calc(100% - 20px); box-sizing: border-box;">
          <!-- Improved title visibility -->
          <h2 class="post-teaser__title" style="margin: 0; font-size: 1.8em; font-weight: bold; text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);">{{ post.title }}</h2>
          <!-- Subtitle styling -->
          <h3 class="post-teaser__subtitle" style="margin-top: 5px; font-size: 1.3em;">{{ post.subtitle }}</h3>
        </div>
      </a>
    </li>
    {% endfor %}
  </ul>
</div>
