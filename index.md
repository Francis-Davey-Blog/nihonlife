---
title: Welcome
layout: default
---
For more than half a century, I rarely travelled beyond the shores of Great Britain, and had no experience of living outside my home culture. Now I find myself settled in Japan. The experience has been interesting. Perhaps I can share some of it with you. Life being what it is, I will not be posting regularly and may mix stories from early in my time here with the day's events.

***
{% for post in site.posts %}
<h2 class="post-title"><a href="{{ post.url | relative_url}}">{{ post.title }} {{ post.date | date: "%e %B %Y" }} </a></h2>
{% if post.subtitle %}
<h3 class="post-subtitle">{{post.subtitle}}</h3>
{% endif %}
{{ post.content | markdownify | strip_html | truncatewords: 50 }}
<a href="{{ post.url | relative_url}}">... read more</a>
{% endfor %}
