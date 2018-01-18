---
layout: archive
permalink: /research/
title: "Research"
author_profile: true
---

知识边界，开疆拓土。

<!-- {% for post in site.research %}
  {% include archive-single.html %}
{% endfor %} -->

<ul>
  {% for post in site.research %}
    {% unless post.next %}
      <font color="#778899"><h2>{{ post.date | date: '%Y %b' }}</h2></font>
    {% else %}
      {% capture year %}{{ post.date | date: '%Y %b' }}{% endcapture %}
      {% capture nyear %}{{ post.next.date | date: '%Y %b' }}{% endcapture %}
      {% if year != nyear %}
        <font color="#778899"><h2>{{ post.date | date: '%Y %b' }}</h2></font>
      {% endif %}

    {% endunless %}
   {% include archive-single.html %}
  {% endfor %}
</ul>