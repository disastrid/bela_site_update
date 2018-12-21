---
layout: resources
section_id: resources
title: Learning Resources
hero-image: ../education/breadboard-2.jpg
---

Bela is designed to make it easy to get started with low-latency interaction, regardless of previous experience with electronics and coding. Our user community goes beyond engineers to include musicians, artists, audio enthusiasts, designers and more, and our online resources help everyone learn, make, and share more.



<div class="full">
  <div class="row flex">
    <div class="large-12 threeimagebox columns bg-grey resource-container">
      {% for item in site.data.resources %}
      <div class="large-3 column resource">
        <div class="resource title"><a href="{{ item.url }}" target="_blank">{{ item.name }}</a></div>
        <p>{{ item.desc }}</p>
        <a href="{{ item.url }}" target="_blank" class='button large'>Go to {{ item.name }} <i class='fas fa-arrow-right'></i></a>
      </div>
      {% endfor %}
    </div>
    <div class='two spacing'></div>
  </div>
</div>