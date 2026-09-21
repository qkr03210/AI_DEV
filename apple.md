---
layout: page
title: "🍎 애플 & 아이패드"
permalink: /apple/
---

디시인사이드 아이패드 갤러리 및 애플 커뮤니티의 실시간 신제품 루머, 특가 핫딜, 유저 팁, 핫이슈 모음입니다.

<ul>
{% assign apple_posts = site.posts | where_exp: "item", "item.categories contains '애플제품' or item.categories contains '아이패드'" %}
{% if apple_posts.size > 0 %}
  {% for post in apple_posts %}
    <li style="margin-bottom: 12px;">
      <span style="color: #666; font-size: 0.9em;">{{ post.date | date: "%Y-%m-%d" }}</span> &nbsp;
      <a href="{{ post.url | relative_url }}" style="font-size: 1.05em; font-weight: 500;">{{ post.title }}</a>
    </li>
  {% endfor %}
{% else %}
  <p style="color: #777;">등록된 애플/아이패드 소식이 없습니다. (첫 수집 완료 후 표시됩니다.)</p>
{% endif %}
</ul>
