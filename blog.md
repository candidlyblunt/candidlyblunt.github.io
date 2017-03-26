---
layout: default
title: blog
permalink: /blog/
weight : 1
---

<br/>
<br/>

<div class="home">
  <h1 class="page-heading">Posts</h1>
  <ul class="post-list">
  
    {% for post in site.posts %}
      <li>
        <span class="post-meta" style="font-family: 'SpecialElite';">{{ post.date | date: "%b %-d, %Y" }}</span>
        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}" style="font-family: 'SpecialElite';">{{ post.title }}</a>
        </h2>
          <article class="post-content">{{ post.content | truncatewords:25}}</article> <br/>
           <a href="{{ post.url }}">Read more...</a>
      
    {% endfor %}
  </ul>
</div>
