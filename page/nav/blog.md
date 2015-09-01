---
layout: navpage
title: Blog
groups: nav
permalink: /blog/
---

<div class="home">

  <ul class="post-list">
    <div class="post_header_blank"></div>
    <!--hr class="hrstyle">
    <div class="post_header_blank"></div-->
    {% for post in site.categories.blog %}
      <!--  div class="general_block"  -->
      <div>
        <li>
          <h2 class="my-post-title">
              <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
          </h2>
          <span class="post-meta">
            Post by <a href="/about/">{{ site.author }}</a> 
            at {{ post.date | date: '%Y-%m-%d' }} 
            with tags 
            {% for tag in post.tags %}
              <a href="{{ site.tags_path }}#{{ tag }}" rel="nofollow">
                {{ tag }}
              </a>
              {% if forloop.last %}
              {% else %}, {% endif %}
            {% endfor %}
          </span>
          <br>
          <p class="my-abstract"> [摘要] {{ post.abstract }} </p>
        </li>
      </div>
      <div class="post_header_blank"></div>
      <hr class="hrstyle">
      <div class="post_header_blank"></div>
    {% endfor %}

  </ul>

  <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>

</div>
