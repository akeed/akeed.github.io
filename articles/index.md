---
layout: page
title: Sample Articles
image:
  feature: so-simple-sample-image-2.jpg
  credit: WeGraphics
excerpt: "An archive of articles sorted by date."
---

<ul class="post-list">
{% for post in site.categories.articles %} 
  <li><article><a href="{{ site.url }}{{ post.url }}">{{ post.title }} <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time></span></a></article></li>
{% endfor %}
</ul>
