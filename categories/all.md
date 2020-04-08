---
layout: page
title: Moje projekty
permalink: /projekty/
---
 

<h1>  {{ page.title }} </h1>

<div class="container row">
{% for projekt in site.projects %}
    <!--PROJECT-->
    <div class="card blog-post">
      <!--THUMBNAIL-->
      <a href="{{ site.categories[projekt][0].url }}" data-disqus-identifier="{{ post.url }}" >
        <img class="card-img-top" src="{{site.url}}{{site.baseurl}}/img/blog/{{ site.categories[projekt][0].thumbnail }}">
      </a>
      <!--TITLE-->
      <div class="card-body center">
        <!--TITLE-->
        <h4 class="card-title">{{ projekt | capitalize }}</h4>
        {% for post in site.categories[projekt] limit:5 %}
          <h6 class="card-subtitle mb-2 "><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h6>
        {% endfor %}
        <!--<a href="{{ post.url | prepend: site.baseurl }}" data-disqus-identifier="{{ post.url }}" class="btn btn-primary btn-lg">Read</a>-->
      </div>
    </div>     
{% endfor %}
</div>
