---
layout: archive
permalink: /year-archive/
title: "作品年表"
author_profile: true
---

<ul class="archive-post-list">
{% assign postsALL = site.posts | concat: site.tools | concat: site.research %}
   {% for post in postsALL %}
       {% assign currentDate = post.date | date: "%Y" %}
       {% if currentDate != myDate %}
           {% unless forloop.first %}</ul>{% endunless %}
           <h1>{{ currentDate }}</h1>
           <ul>
           {% assign myDate = currentDate %}
       {% endif %}
        <li class="listing-item">
            <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
        <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
        </li>
   {% endfor %}
</ul>

<!-- 
<ul class="listing">
{% assign postsALL = site.posts | concat: site.tools | concat: site.research %}
{% for post in postsALL %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <li class="listing-seperator">{{ y }}</li>
  {% endif %}
  <li class="listing-item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>

{% endfor %}

</ul> -->

<!-- {% assign postsByYear = site.posts | group_by_exp:"post", "post.date | date: '%Y'"  %}
{% for year in postsByYear %}
  <h2 id="{{ year.name | slugify }}" class="archive__subtitle">{{ year.name }}</h2>
  {% for post in year.items %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %} -->