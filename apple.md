---
layout: page
title: "🍎 애플 & 아이패드"
permalink: /apple/
---

디시인사이드 아이패드 갤러리 및 애플 커뮤니티의 실시간 신제품 루머, 특가 핫딜, 유저 팁, 핫이슈 모음입니다.

<ul>
{% for post in site.posts %}
  {% if post.categories contains '애플제품' or post.categories contains '아이패드' %}
    <li style="margin-bottom: 12px;">
      <span style="color: #666; font-size: 0.9em;">{{ post.date | date: "%Y-%m-%d" }}</span> &nbsp;
      <a href="{{ post.url | relative_url }}" style="font-size: 1.05em; font-weight: 500;">{{ post.title }}</a>
    </li>
  {% endif %}
{% endfor %}
</ul>
