---
title: "News"
layout: textlay
excerpt: "GVD Lab at Ontario Tech University."
sitemap: false
permalink: /allnews.html
---

# News from Graphics and Virtual Dynamics Lab

{% for article in site.data.news %}

### {{ article.date | markdownify | strip_html }} 

{{ article.headline | markdownify}}

{% if article.image %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/newspic/{{ article.image }}" class="img-responsive" width="50%" />
{% endif %}

{% endfor %}
