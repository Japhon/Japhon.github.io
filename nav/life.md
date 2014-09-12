---
layout: default
title: 生活
---

<div class="home cc">
  <div class="introhead">
    <h1 class="page-heading"></h1>
    <img class="intro" src="/photo/portrait.jpg" width="85" height="85" />
    <p class="intro"><i>Japhon是一个热爱生活的人。生活中总会有很多有趣的事情。开心其实很简单，有时候可能是因为一餐饭，有时候可能是因为一首歌，有时候可能是因为一个眼神，有时候可能是因为旅行途中的一点小感动。生活就是要这样，平平凡凡，在简简单单中寻找快乐。你觉得呢？</i></p>
  </div>
  <hr />
  {% for post in site.categories.life %}
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
