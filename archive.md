---
layout: page
title: archive
permalink: /archive/
weight : 2
---

<section id="archive">
  <h3>This year's posts</h3>
  {%for post in site.posts %}
    {% unless post.next %}
      <ul class = "this" style="list-style: none;">
    {% else %}
      {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
      {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
      {% if year != nyear %}
        </ul>
        <br>
        <h3>{{ post.date | date: '%Y' }}</h3>
        <ul class="past" style="list-style: none; text-align:center;">
      {% endif %}
    {% endunless %}
      <li><time>{{ post.date | date:"%d %b" }}</time><a href="{{ post.url }}"> {{ post.title }}</a>
       <br></li>

  {% endfor %}
  </ul>
</section>