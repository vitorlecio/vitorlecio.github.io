---
layout: page
#title: Blog
#subtitle: Select ramblings of Pudhina
---

<div>
<ul class="list-posts">
  {% for post in site.posts %}
  <li class="post-teaser" style="display: flex; align-items: center; margin-bottom: 20px;">
    <a href="{{ post.url | prepend: site.baseurl }}" style="display: flex; align-items: center; text-decoration: none;">
      <!-- Post-specific image -->
      <div style="flex-shrink: 0; margin-right: 20px;">
        <img src="{{ post.image | prepend: site.baseurl }}" id="post-img" style="width: 200px; height: auto;">
      </div>
      <!-- Post text content -->
      <div style="color: black;">
        <h2 class="post-teaser__title" style="margin: 0;">{{ post.title }}</h2>
        <p class="post-teaser__excerpt">{{ post.excerpt }}</p>
      </div>
    </a>
  </li>
  {% endfor %}
</ul>
</div>
