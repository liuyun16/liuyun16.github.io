---
layout: archive
permalink: /tools/
title: "Tools"
author_profile: true
---

化学人也能懂得一些软件应用、编程技术

<!-- <ul>
  {% for post in site.tools %}
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
</ul> -->

{% for post in site.tools %}
  {% include archive-single.html %}
{% endfor %}