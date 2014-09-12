---
layout: default
title: 杂文
---

<div class="home bb">
  <div class="introhead">
    <h1 class="page-heading"></h1>
    <img class="intro" src="/photo/portrait.jpg" width="85" height="85" />
    <p class="intro"><i>Japhon是一个很喜欢把自己的想法和大家分享的人。有时候看到新闻或者一些资讯，都免不了自己赞同或者吐槽一番。我希望在吐槽的时候也可以听一听大家的看法。如果大家看了文章觉得很有同感的话，需要转载的话，如果能注明一下出处，那就再好不过了！谢谢大家！</i></p>
  </div>
  <hr />
  {% for post in site.categories.essay %}
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
