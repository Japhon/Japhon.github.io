---
layout: navpage
title: Article
groups: nav
permalink: /article/
---

<div class="home">

  <ul>
    <div class="post_header_blank"></div>
    <!--hr class="hrstyle">
    <div class="post_header_blank"></div-->
    {% for post in site.posts %}
      <!--  div class="general_block"  -->
      <div>
        <li>
          <span class="post-meta">
            <a class="article-meta" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a> &#009;{{ post.date | date: '%Y-%m-%d' }} 
          </span>
        </li>
      </div>
      <!--
      <div class="post_header_blank"></div>
      <hr class="hrstyle">
      <div class="post_header_blank"></div>
    -->
    {% endfor %}

  </ul>

  <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>

</div>
