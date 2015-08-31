---
layout: page
title: Tags
groups: no-nav
permalink: /tags/
---

<div class="home">
  <div class="general_block">
    <div class="tags_home">
      {% for tag in site.tags %}
        <a class="tags_block_link" href="#{{ tag[0] }}">
          <div class="tags_block"> {{ tag[0] }} <SUP> {{ tag[1].size }} </SUP></div>
        </a> 
      {% endfor %}
    </div>
    <div class="clear-float"></div><!-- this one is the line for clear the left float-->
  </div>

  {% for tag in site.tags %}
    <div id="{{ tag[0] }}" class="general_block">
      <h3>{{ tag[0] }}</h3>
      <ul>
        {% for post in tag[1] %}
          <li class="tags_post_list">
            <a href="{{ post.url | prepend: site.baseurl }}"> {{ post.title }} - <span class="post-meta">{{ post.date | date: "%Y-%-m-%-d" }}</span></a>
          </li>
        {% endfor %}
      </ul>
    </div>
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

</div>
