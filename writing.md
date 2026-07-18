---
layout: default
title: Writing
permalink: /writing/
---
<section class="page-heading"><p class="eyebrow">Writing</p><h1>Notes and explanations.</h1><p class="lede">Blog posts, expository mathematics, and attempts to make difficult things clearer.</p></section>
{% assign writing = site.posts | concat: site.articles | sort: 'date' | reverse %}
<section class="writing-section"><div class="writing-list">{% for item in writing %}<article><p class="date">{{ item.date | date: "%d %B %Y" }}</p><h3><a href="{{ item.url | relative_url }}">{{ item.title }}</a></h3>{% if item.excerpt %}<p>{{ item.excerpt | strip_html | truncatewords: 32 }}</p>{% endif %}</article>{% endfor %}</div></section>
