---
layout: product-page
section_id: products
hero-image: /products/hero-trill.png
title: Trill Touch Sensors
sub-title: Capacitive touch sensing inspired by musicians, designed for makers
permalink: /products/trill/
---

Trill is a family of touch sensors designed to place the power of high-resolution touch sensing in the hands of artists, designers, musicians, and creative makers embarking upon elevated interactive projects

There are six Trill types, all designed by the team that brought you Bela but compatible with a wide range of systems such as Arduino, Teensy and Raspberry Pi. Download the Trill library and example projects for Bela and other platforms in the <a href="https://learn.bela.io/products/trill/about-trill/">Bela Knowledge Base</a>.

{% for item in site.data.product_list.trill %}
<div class='row product-item'>
    <div class='medium-4 columns'>
      <img class="fadeinleft" alt="" src="{{ site.baseurl }}/images/products/trill/{{ item.image }}"/>
    </div>
    <div class='medium-8 columns'>
      <div class='spacing'></div>
      <h2>{{ item.title }}</h2>
      <div class='spacing'></div>
      <p>{{ item.desc }}</p>
      <div class='spacing'></div>
      <h3>Dimensions: {{ item.dimensions }}</h3>
      <a class='button buy' href="{{ item.url }}" target='_blank'>Buy {{ item.title }} now <i class='fas fa-arrow-right'></i></a>
  </div>
</div>
{% endfor %}

