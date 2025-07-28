---
title: "News"
layout: textlay
excerpt: "GVD Lab at Ontario Tech University."
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}

{{ article.date }} <br> {{ article.headline | markdownify}}

{% endfor %}
