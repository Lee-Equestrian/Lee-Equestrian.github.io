---
layout: page
title: Performance Horses
permalink: /performancehorses
---
<div class="container p-3">
  <div class="row justify-content-center">
    <!-- for loop -->
    {% assign horse_order = site.categories.performance | sort: 'order' %}
    {% for horse in horse_order %}
    <!-- Card Container -->
    <div class="col-12 col-md-6 col-lg-4 col-xl-3 py-2 mx-auto ">
      <div class="card d-block mx-auto" style="border: 0;">
        <header class="card-personal-header" style="background: url('{{site.baseurl}}{{horse.card-img}}');">
          <h4 class="card-personal-name">{{horse.title}}</h4>
          <p class="card-personal-description">
            {% assign horse-pedigree = horse.pedigree.sire.name | append: " + " | append: horse.pedigree.dam.sire.name %}
            {{horse-pedigree}}      
          </p>
        </header>
        <section class="card-personal-info">
          <a href="{{site.baseurl}}{{horse.url}}">Visit Page</a>
          <a href="{{site.baseurl}}{{horse.url}}#pictures">View Pictures</a>
        </section>
      </div>
    </div>
    <!-- Card Container -->
    {% endfor %}
    <!-- End for loop -->
  </div>
</div>