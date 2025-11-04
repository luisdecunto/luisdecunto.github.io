---
layout: page
title: blog
permalink: /blog/
description: Technical articles on machine learning, numerical methods, and engineering
nav: true
nav_order: 3
pagination:
  enabled: true
  collection: posts
  permalink: /page/:num/
  per_page: 5
  sort_field: date
  sort_reverse: true
  trail:
    before: 1
    after: 3
---

<div class="posts">

{%- for post in paginator.posts %}
  <div class="post-preview">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p class="post-meta">
      {{ post.date | date: "%B %-d, %Y" }}
      {%- if post.author %}
        • <span>{{ post.author }}</span>
      {%- endif %}
    </p>
    <p>{{ post.description }}</p>
    <div class="post-tags">
      {%- for tag in post.tags %}
        <a href="{{ '/blog/tag/' | append: tag | relative_url }}" class="badge badge-pill badge-primary">{{ tag }}</a>
      {%- endfor %}
    </div>
  </div>
{%- endfor %}

<!-- Pagination links -->
{%- if paginator.total_pages > 1 %}
<nav aria-label="Page navigation">
  <ul class="pagination justify-content-center">
    {%- if paginator.previous_page %}
    <li class="page-item">
      <a class="page-link" href="{{ paginator.previous_page_path | relative_url }}">&laquo; Prev</a>
    </li>
    {%- else %}
    <li class="page-item disabled">
      <span class="page-link">&laquo; Prev</span>
    </li>
    {%- endif %}

    {%- for page in (1..paginator.total_pages) %}
      {%- if page == paginator.page %}
      <li class="page-item active">
        <span class="page-link">{{ page }}</span>
      </li>
      {%- elsif page == 1 %}
      <li class="page-item">
        <a class="page-link" href="{{ '/blog/' | relative_url }}">{{ page }}</a>
      </li>
      {%- else %}
      <li class="page-item">
        <a class="page-link" href="{{ '/blog/page/' | append: page | relative_url }}">{{ page }}</a>
      </li>
      {%- endif %}
    {%- endfor %}

    {%- if paginator.next_page %}
    <li class="page-item">
      <a class="page-link" href="{{ paginator.next_page_path | relative_url }}">Next &raquo;</a>
    </li>
    {%- else %}
    <li class="page-item disabled">
      <span class="page-link">Next &raquo;</span>
    </li>
    {%- endif %}
  </ul>
</nav>
{%- endif %}

</div>
