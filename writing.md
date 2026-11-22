---
layout: page
title: Writing
permalink: /writing/
---

{% assign writing_posts = site.posts | where_exp: "post", "post.categories contains 'writing'" %}
{% for post in writing_posts %}

### [{{ post.title }}]({{ post.url | relative_url }})
{{ post.date | date: "%B %-d, %Y" }}

{% endfor %}
