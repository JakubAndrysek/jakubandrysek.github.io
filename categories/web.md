---
layout: page
title: Web
permalink: /blog/categories/web
---
 
<h5> Posts by Category : {{ page.title }} </h5>

<div class="card">
{% for post in site.categories.web %}
 <li class="category-posts"><span>{{ post.date | date: "%d. %m. %Y" }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</div>