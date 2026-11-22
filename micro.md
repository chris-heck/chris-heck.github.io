---
layout: page
title: Micro
permalink: /micro/
---

<p>Short observations, links, and everyday moments.</p>

## From this blog

{% assign micro_posts = site.posts | where_exp: "post", "post.categories contains 'micro'" %}
{% for post in micro_posts %}
{% if post.title and post.title != "" %}
### [{{ post.title }}]({{ post.url | relative_url }})
{% endif %}
[{{ post.date | date: "%B %-d, %Y" }}]({{ post.url | relative_url }})

{{ post.content }}

---
{% endfor %}

## From Micro.blog

<script src="https://micro.blog/sidebar.js?username=chrisheck&count=25"></script>