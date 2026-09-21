---
layout: page
title: "🎲 보드게임 & 이슈"
permalink: /boardgames/
---

보드라이프(신작·펀딩·출시 소식) 및 디시인사이드 갤러리(화제의 개념글)의 일일 정리 모음입니다.

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
  <p style="color: #777;">아직 등록된 보드게임 소식이 없습니다. (오늘 일일 정리 작업이 완료되면 등록됩니다.)</p>
{% endif %}
</ul>
