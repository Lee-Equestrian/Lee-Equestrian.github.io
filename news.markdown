---
layout: page
title: Latest News
permalink: /news
---
<div class="container">
<ul>
    {% for news in site.categories.news %}
    <li>
        <a href="{{news.url}}">{{news.title}}</a>
        <p>{{news.meta}}</p>
    </li>
    {% endfor %}
</ul>
</div>