---
layout: product-page
section_id: products
hero-image: trill_hero.png
title: Trill touch sensors
sub-title: Capacitive touch sensing inspired by musicians, designed for makers
permalink: /products/trill
---

Trill is a family of touch sensors designed by Bela. Launched in 2019 on Kickstarter, Trill is designed to place the power of high-resolution touch sensing in the hands of artists, designers, musicians, and creative makers of all kinds. 

<a href='https://www.kickstarter.com/projects/423153472/trill-touch-sensing-for-makers?ref=5h34wt&token=6b96b598'>Launched on Kickstarter in 2019</a>, Trill was inspired by the way we use our hands to interact with the world. Harnessing the power of capacitive touch for interaction, Trill sensors offer a range of shapes, sizes and interaction types to bring touch sensing to any interactive project.

{% include youtube.html id='xzaf2bBKuQI' %}

<h2>For natural, beautiful touch sensing</h2>

From computer interfaces to textiles, musical instruments to interactive artworks, getting touch right in the design of objects and products is essential to get right. Trill touch sensors are high-resolution touch sensors, designed for makers, that are easy to integrate into any interactive project.

There are five types of Trill sensor: Bar, Square, Craft, Hex and Ring. Bar and Ring are multi-touch sliders, Square and Hex are x/y sensors, and Craft allows you to make any kind touch interface you can imagine, out of any conductive material. 

{% include threeimage.html path='/products/trill/' one='bar_ani.gif' two='square_ani.gif' three='craft_ani.gif' %}

<h2>Designed for Bela, widely compatible</h2>

Trill sensors were designed to take advantage of Bela's low-latency capabilities, but are compatible with any system or microcontroller that supports I2C communication such as Arduino, Raspberry Pi or Teensy. Libraries and examples for other platforms are available on <a href="https://github.com/belaPlatform/trill">our Github repo</a>.

<div class='spacing two'></div>

<h2>Types of Trill sensors</h2>

{% for sensor in site.data.product_list.trill %}
<div class='row product-item'>
    <div class='medium-4 columns'>
      <img class="fadeinleft" alt="" src="{{ site.baseurl }}/images/products/trill/{{ sensor.image }}"/>
    </div>
    <div class='medium-8 columns'>
      <div class='spacing'></div>
      <h2>{{ sensor.title }}</h2>
      <div class='spacing'></div>
      <p>{{ sensor.desc }}</p>
      <h3>Dimensions: {{ sensor.dimensions }}</h3>
      <a class='button buy' href="{{ item.url }}" target='_blank'>Buy {{ sensor.title }} now <i class='fas fa-arrow-right'></i></a>
  </div>
</div>
{% endfor %}