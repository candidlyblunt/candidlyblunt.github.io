---
layout: page
title: archive
permalink: /archive/
---

<section id="archive" align = "left">
  <h3>This year's posts</h3>
  {%for post in site.posts %}
    {% unless post.next %}
      <ul style="list-style-type:none">

    {% else %}
      {% capture year %} {{ post.date | date: '%Y' }} {% endcapture %}

      {% capture nyear %} {{ post.next.date | date: '%Y' }} {% endcapture %}
      {% if year != nyear %}
        </ul>
        <h3>  {{| post.date | date: '%Y' }} &nbsp;</h3>
        <ul class="past">
      {% endif %}
    {% endunless %}

      <li><time>  {{ post.date | date:"%d %b" }} &nbsp;</time><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
  </ul>
</section>

