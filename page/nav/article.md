---
layout: navpage
title: Article
groups: nav
permalink: /article/
---

<div class="home">
  <ul class="post-list">
    <div class="post_header_blank"></div>
    <li>
      <h2 class="my-post-title">全部文章</h2>
    </li>
  </ul>

  <ul class="article-list">
    <div class="post_header_blank"></div>
    <!--hr class="hrstyle">
    <div class="post_header_blank"></div-->
    {% for post in site.posts %}
      <!--  div class="general_block"  -->
      <div>
        <li>
          <span class="post-meta">
            <a class="article-meta" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a> {{ post.date | date: '%Y-%m-%d' }} 
          </span>
        </li>
      </div>
      

      <hr class="hrstyle">

    
    {% endfor %}

  </ul>

  <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>

</div>
