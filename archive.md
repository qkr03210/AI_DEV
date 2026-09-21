---
layout: page
title: "🗄️ 전체 보관함"
permalink: /archive/
---

지금까지 발행된 모든 게시글 목록입니다.

<ul>
{% for post in site.posts %}
  <li style="margin-bottom: 10px;">
    <span style="color: #666; font-size: 0.88em;">{{ post.date | date: "%Y-%m-%d" }}</span> &nbsp;
    <span style="background: #eef; color: #33a; padding: 2px 6px; border-radius: 4px; font-size: 0.8em;">{{ post.categories | join: ', ' }}</span> &nbsp;
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
