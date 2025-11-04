---
layout: page
title: Blog
permalink: /blog/
---

Technical articles on machine learning, numerical methods, and engineering.

{%- for post in site.posts %}
## [{{ post.title }}]({{ post.url | relative_url }})
*{{ post.date | date: "%B %-d, %Y" }}*

{{ post.description }}

---
{%- endfor %}
