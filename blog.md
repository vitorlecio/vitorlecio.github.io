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

<div style="display: flex;"> 
<div style="flex: 1; background-color: lightblue;"><img src="{{ '/assets/img/profile.jpeg' | prepend: site.baseurl }}" id="about-img"></div>
<!--img src="post-teaser__title">{{post.logo}}-->
<div style="flex: 1; background-color: lightgreen;"><span class="post-teaser__title">{{ post.title }}</span></div> 
</div>
<!--span class="post-teaser__date">{{ post.date | date: "%d %B %Y" }}</span -->

</a>

</li>
{% endfor %}
</ul>
{% endfor %}
</div>