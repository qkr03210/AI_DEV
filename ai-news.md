---
layout: page
title: "🤖 AI 테크 브리핑"
permalink: /ai-news/
---

최신 인공지능(AI) 트렌드와 매일 수집되는 모닝 브리핑 글 모음입니다.

<ul>
{% for post in site.posts %}
  {% if post.categories contains 'AI뉴스' or post.categories contains '인공지능' %}
    <li style="margin-bottom: 12px;">
      <span style="color: #666; font-size: 0.9em;">{{ post.date | date: "%Y-%m-%d" }}</span> &nbsp;
      <a href="{{ post.url | relative_url }}" style="font-size: 1.05em; font-weight: 500;">{{ post.title }}</a>
    </li>
  {% endif %}
{% endfor %}
</ul>
