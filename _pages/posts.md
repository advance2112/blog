---
title: "Posts"
permalink: /posts/
layout: archive
search: true
---

{% for post in site.posts %}
  {% include posts-list.html %}
{% endfor %}