---
layout: page
#title: Blog
#subtitle: Select ramblings of Pudhina
---

<div>
{% assign postsCategory = site.posts | group_by_exp:"post", "post.categories"  %}
{% for category in postsCategory %}
<h4 class="post-teaser__month">
<strong>
{% if category.name %} 
- - - - -  {{ category.name }} - - - - - 
{% else %} 
{{ Print }} 
{% endif %}
</strong>
</h4>
<ul class="list-posts">
{% for post in category.items %}
<li class="post-teaser">
<a href="{{ post.url | prepend: site.baseurl }}">
       <div style="position: relative; width: 100%; max-width: 400px;">
          <!-- Post-specific image -->
          <img src="{{ post.image | prepend: site.baseurl }}" id="post-img" style="width: 100%; height: auto;">
          <!-- Title overlay -->
          <div style="position: absolute; bottom: 0; background: rgba(0, 0, 0, 0.5); color: white; width: 100%; text-align: center;">
            <span class="post-teaser__title">{{ post.title }}</span>
            </div>
          </div>
        </a>

</li>
{% endfor %}
</ul>
{% endfor %}
</div>