---
layout: page
title: Geldings
permalink: /geldings
---
<div class="container">
<ul>
    {% for horse in site.categories.geldings %}
    <li>
        <a href="{{horse.url}}">{{horse.title}} | {{horse.title}}</a>
        <p>{{horse.meta}}</p>
    </li>
    {% else %}
    <div class="row text-center p-2">
    <div class="col">
    <h1>Sorry!</h1>
    <p><strong>Geldings not found :(</strong></p>
    <p>We currently do not have any geldings in development.</p>
    <img src="{{site.baseurl}}/assets/img/illustrations/faq.svg" style="width: 256px">
    </div>
    </div>
    {% endfor %}
</ul>
</div>