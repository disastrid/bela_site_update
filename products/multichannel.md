---
layout: product-page
section_id: products
hero-image: /products/hero-multichannel.jpg
title: Multichannel
sub-title: Take your audio to the next level
permalink: /products/multichannel/
---

<div class='row product-section'>
    {% for item in site.data.product_list.accessories %}
    <div class='row product-item'>
    <div class='medium-4 columns'>
        <img class="fadeinleft" alt="" src="{{ site.baseurl }}/images/products/{{ item.image }}"/>
    </div>
    <div class='medium-8 columns'>
        <div class='spacing'></div>
        <h2>{{ item.title }}</h2>
        <h4 class="text-light-grey">{{ item.superheading }}</h4>
        <div class='spacing'></div>
        <p>{{ item.desc }}</p>
        <div class='spacing'></div>
        {% if item.specs %}
        <ul class='shortcode-list'>
        {% for thing in item.specs %}
        <li>
            <i class='fa fa-check'></i>
            {{ thing.spec }}
        </li>
        {% endfor %}
        </ul>
        {% endif %}
        <div class='spacing'></div>
        <a class='button large page-scroll' href='{{ item.url }}' target='_blank'>{% if item.title == "Trill Touch Sensors" %}Learn More {% else %}Buy now {% endif %}<i class='fas fa-arrow-right'></i></a>
    </div>
    </div>
    {% endfor %}
</div>