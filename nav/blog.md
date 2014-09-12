---
layout: default
title: 博客
permalink: /home_page/
---
<!--For the catalogue-->

<div class="home aa">
  <div class="introhead">
    <h1 class="page-heading"></h1>
    <img class="intro" src="/photo/portrait.jpg" width="85" height="85" />
    <p class="intro"><i>Japhon来自于广州国立中山大学软件学院，数字媒体专业。非典型程序猿。这个技术博客，用来记录下平常学习到的点点滴滴，或者是碰到的问题。希望可以和同样是这方面的爱好者相互学习交流。如果对于文章中有什么问题，欢迎大家在下面留言指出。谢谢大家！</i></p>
  </div>
  <hr />
  {% for post in site.categories.blog %}
    <a href="{{ post.url | prepend: site.baseurl }}">
      <li>
        <h2>
          <center><div class="post-link"> {{ post.title }} </div></center>
          <center><span class="post-meta"> {{ post.date | date: "%b %-d, %Y" }} </span></center>
        </h2>
        <span class="post-meta"> [摘要] </span><span> {{ post.abstract }} </span><span class="post-meta"> [查看全文] </span>
      </li>
    </a>
    <hr />
  {% endfor %}
</div>
