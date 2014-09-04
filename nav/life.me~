---
layout: default
title: 生活
---

<div class="home">
  <h1 class="page-heading"></h1>
  {% for post in site.categories.life %}
    <a href="{{ post.url | prepend: site.baseurl }}">
      <li>
        <h2>
          <center><div class="post-link"> {{ post.title }} </div></center>
          <center><span class="post-meta"> {{ post.date | date: "%b %-d, %Y" }} </span></center>
        </h2>
       <span> [摘要] {{ post.abstract }} </span>
      </li>
    </a>
  {% endfor %}
</div>
