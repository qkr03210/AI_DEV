---
layout: page
title: "🎲 보드게임 레이더"
permalink: /boardgames/
---

보드라이프(신작·출시·펀딩)와 디시인사이드 부루마불 갤러리(커뮤니티 이슈)의 종합 일일 브리핑입니다.

<ul>
{% assign bg_posts = site.posts | where_exp: "item", "item.categories contains '보드게임'" %}
{% if bg_posts.size > 0 %}
  {% for post in bg_posts %}
    <li style="margin-bottom: 12px;">
      <span style="color: #666; font-size: 0.9em;">{{ post.date | date: "%Y-%m-%d" }}</span> &nbsp;
      <a href="{{ post.url | relative_url }}" style="font-size: 1.05em; font-weight: 500;">{{ post.title }}</a>
    </li>
  {% endfor %}
{% else %}
  <p style="color: #777;">등록된 보드게임 소식이 없습니다.</p>
{% endif %}
</ul>
