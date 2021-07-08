---
layout: product-page
section_id: default
hero-image: /products/hero-bela.jpg
title: Bela and Bela Mini
sub-title: Change how you interact with audio, forever.
permalink: /products/bela-and-bela-mini/
---

{% for item in site.data.product_list.boards %}
<div class='row product-item'>
    <div class='medium-4 columns'>
        <img class="fadeinleft" alt="" src="{{ site.baseurl }}/images/products/{{ item.image }}" target='_blank'/>
    </div>
    <div class='medium-8 columns'>
        <h2 class="product-title">{{ item.title }}</h2>
        <p>{{ item.desc }}</p>
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
        <a class='button large' href='{{ item.url }}'  target='_blank'>Buy now <i class='fas fa-arrow-right'></i></a>
        <div class='two spacing'></div>
    </div>
</div>
{% endfor %}
<div class="two spacing"></div>
