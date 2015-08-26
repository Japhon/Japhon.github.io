---
layout: navpage
title: 博客
groups: nav
permalink: /blog/
---

<div class="home">

  <ul class="post-list">
    {% for post in site.categories.blog %}
      <div class="general_block">
        <li>
          <h2>
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
    {% endfor %}
  </ul>

  <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>

</div>
