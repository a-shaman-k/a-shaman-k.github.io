---
layout: default
title: Home
---
<section class="hero"><p class="eyebrow">Personal website</p><h1>Making the world<br>less fuzzy.</h1><p class="lede">I write to think: about mathematics, ideas, and the things worth understanding.</p><p><a class="button" href="{{ '/writing/' | relative_url }}">Read my writing</a></p></section>
<section class="home-grid"><div><p class="eyebrow">About</p><h2>A little about me</h2><p>Find my background, a short introduction, and my CV.</p><a href="{{ '/about/' | relative_url }}">More about me →</a></div><div><p class="eyebrow">Latest writing</p>{% assign latest = site.posts.first %}{% if latest %}<h2><a href="{{ latest.url | relative_url }}">{{ latest.title }}</a></h2><p>{{ latest.excerpt | strip_html | truncatewords: 24 }}</p><a href="{{ '/writing/' | relative_url }}">All writing →</a>{% else %}<h2>Writing is on its way.</h2>{% endif %}</div></section>
