---
title: "News"
layout: textlay
excerpt: "GVD Lab at Ontario Tech University."
sitemap: false
permalink: /allnews.html
---

# News from Graphics and Virtual Dynamics Lab

{% for article in site.data.news %}

{{ article.date }} <br> {{ article.headline | markdownify}}

{% endfor %}

{% assign number_printed = 0 %}
{% for article in site.data.news %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-12 clearfix">
 <div class="well">
  <pubtit>{{ article.headline }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/newspic/{{ article.image }}" class="img-responsive" width="50%" style="float: left" />
  <p>{{ article.date }}</p>  
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
