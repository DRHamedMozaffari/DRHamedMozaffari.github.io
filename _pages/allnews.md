---
title: "News"
layout: page
permalink: /news/
---

# News

{% if site.data.news and site.data.news.size > 0 %}
<div class="section-card" markdown="0">
<div class="news-timeline">
{% for article in site.data.news %}
<div class="news-item">
<span class="news-date">{{ article.date }}</span>
<span class="news-headline">{{ article.headline }}</span>
</div>
{% endfor %}
</div>
</div>
{% else %}
<p class="text-muted">News will be posted here soon. Add entries to <code>_data/news.yml</code>.</p>
{% endif %}
