---
layout: product-page
section_id: products
hero-image: salt_hero.jpg
title: Trill touch sensors
sub-title: Capacitive touch sensing inspired by musicians, designed for makers
permalink: /products/trill
---

Trill is a family of touch sensors designed by Bela. Launched in 2019 on Kickstarter, Trill is designed to place the power of high-resolution touch sensing in the hands of artists, designers, musicians, and creative makers of all kinds.

<h2>For natural, beautiful touch sensing</h2>

Trill was inspired by the way we use our hands to interact with the world. Harnessing the power of capacitive touch for interaction, Trill sensors offer a range of shapes, sizes and interaction types to bring touch sensing to any interactive project.

<h2>Types of Trill sensors</h2>

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
  {% endfor %}

<h2>Designed for Bela, widely compatible</h2>

Though Trill Touch Sensors are designed to take advantage of Bela's high-resolution sensing and low-latency processing, they are compatible with any system that suppports I2C, such as Teensy, Arduino, and Raspberry Pi. Download the Trill library and example projects for Bela and other platforms on <a href="https://github.com/belaPlatform/trill">our Github</a>.