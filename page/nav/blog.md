---
layout: page
title: 博客
groups: nav
permalink: /blog/
---

<div class="home">

  <ul class="post-list">
    {% for post in site.categories.blog %}
      <li>
        <h2>
            <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
        <span class="post-meta">{{ post.date | date: "%Y-%-m-%-d" }}</span><br>
        <p class="my-abstract"> [摘要] {{ post.abstract }} </p>       
      </li>
    {% endfor %}
  </ul>

  <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>

</div>