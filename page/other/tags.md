---
layout: page
title: Tags
groups: no-nav
permalink: /tags/
---

<div class="home">
  <div class="tags_home">
  {% for tag in site.tags %}
    <span><a href="#{{ tag[0] }}"> {{ tag[0] }} </a> </span>
  {% endfor %}
  </div>

  {% for tag in site.tags %}
    <h4 id="{{ tag[0] }}">{{ tag[0] }}</h4>
    <ul>
      {% for post in tag[1] %}
        <li>
          <a href="{{ post.url | prepend: site.baseurl }}"> {{ post.title }} - <span class="post-meta">{{ post.date | date: "%Y-%-m-%-d" }}</span></a>
        </li>
      {% endfor %}
    </ul>
  {% endfor %}

<!-- test
  {% for tag in site.tags %}
    <p>tag: '{{ tag[0] }}',</p>
    <p>freq: {{ tag[1].size }},</p>
    <p>posts: </p>

    {% for post in tag[1] %}
      <p>title: '{{ post.title }}',</p>
      <p>url: '{{ BASE_PATH }}{{ post.url }}',</p>
      <p>date: '{{ post.date | date: "%Y-%m-%d" }}'</p>
    {% endfor %}

  {% endfor %}
-->

<!-- 原post
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
-->

</div>
