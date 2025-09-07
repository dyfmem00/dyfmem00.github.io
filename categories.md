---
layout: default
title: Categories
---

## 모든 카테고리 목록

{% for category in site.categories %}
  <h3 id="{{ category[0] | slugify }}">{{ category[0] }}</h3>
  <ul>
    {% for post in category[1] %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </li>
    {% endfor %}
  </ul>
{% endfor %}