---
layout: default
title: "Gallery"
permalink: /gallery/
---
<div class="page-header">
  <h1>Gallery</h1>
  <p>Click to see full-size images</p>
</div>

<!-- 图片配置区：新增图片仅需在这里按格式加一行 -->
{% assign gallery_list = "
  src:/assets/images/gallery-group-photo.jpg|alt:Group Photo|caption:Group Photo, SPMS-LT1, 11am 21 March 2026
" | strip | newline_to_br | split: "<br />" %}

<!-- 自动渲染所有图片，无需修改下方代码 -->
{% for item in gallery_list %}
  {% assign img_data = item | strip | split: "|" %}
  {% assign src = img_data[0] | split: ":" | last %}
  {% assign alt = img_data[1] | split: ":" | last %}
  {% assign caption = img_data[2] | split: ":" | last %}
<div class="registration-img-container mb-4">
  <a href="{{ src }}" target="_blank" rel="noopener noreferrer">
    <img src="{{ src }}" alt="{{ alt }}" class="registration-img-thumbnail">
  </a>
  <p class="mt-2 text-muted small text-center">{{ caption }}</p>
</div>
{% endfor %}