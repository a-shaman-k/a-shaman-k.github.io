---
layout: default
title: Writing
permalink: /writing/
---
<section class="page-heading"><p class="eyebrow">Writing</p><h1>Notes and explanations.</h1><p class="lede">Blog posts, expository mathematics, and attempts to make difficult things clearer.</p></section>
<section class="writing-section"><h2>Mathematics articles</h2>{% assign articles = site.articles | sort: 'date' | reverse %}{% if articles.size > 0 %}<div class="writing-list">{% for article in articles %}<article><p class="date">{{ article.date | date: "%d %B %Y" }}</p><h3><a href="{{ article.url | relative_url }}">{{ article.title }}</a></h3>{% if article.excerpt %}<p>{{ article.excerpt }}</p>{% endif %}</article>{% endfor %}</div>{% else %}<p class="empty-state">Mathematics articles will appear here.</p>{% endif %}</section>
<section class="writing-section"><h2>Blog posts</h2><div class="writing-list">{% for post in site.posts %}<article><p class="date">{{ post.date | date: "%d %B %Y" }}</p><h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>{% if post.excerpt %}<p>{{ post.excerpt | strip_html | truncatewords: 32 }}</p>{% endif %}</article>{% endfor %}</div></section>
