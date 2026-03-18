---
layout: default
title: "Registration"
permalink: /registration/
---

<!-- 开头信息轻量结构化 - 不照搬卡片，简约排版 -->
<div class="registration-info mb-5">
  <div class="registration-info__item mb-3">
    <span class="registration-info__label">Fee information:</span> the event is <strong>free</strong> to participate
  </div>
  <div class="registration-info__item mb-3">
    <span class="registration-info__label">Capacity limits:</span> ~ 100 people
  </div>
  <!-- <div class="registration-info__item">
    <span class="registration-info__label">Visa support information:</span><br>
    Please check back later, or contact the organizers via the <a href="{{ '/contact/' | relative_url }}">contact page</a>.
  </div> -->
  <div class="registration-info__item mb-3">
    <span class="registration-info__label">Detailed Address of SPMS:</span> School of Physical and Mathematical Sciences, NTU, 21 Nanyang Link, Singapore 637371
  </div>
</div>

<!-- 现场注册标题+表格 - 优化排版 -->
<h2 class="h4 fw-bold text-dark mb-4">On-site Registration</h2>
<p class="mb-3">On-site registration will take place at the <strong>SPMS</strong> (School of Physical and Mathematical Sciences), NTU, during the following times:</p>

<div class="registration-table mb-5">
  <table class="table table-sm table-bordered">
    <thead>
      <tr>
        <th class="text-center">Date</th>
        <th class="text-center">Place</th>
        <th class="text-center">Time</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>18 March 2026 (Wednesday)</td>
        <td>SPMS Atrium (Level 3)</td>
        <td class="text-center">17:00 – 20:00</td>
      </tr>
      <tr>
        <td>19 March 2026 (Thursday)</td>
        <td>SPMS LT1 (Level 4)</td>
        <td class="text-center">08:00 – 09:00</td>
      </tr>
    </tbody>
  </table>
</div>

<!-- 图片：缩略图+点击放大模态框 -->
<h3 class="h5 fw-medium text-dark mb-3">SPMS Main Entrance</h3>
<div class="registration-img-container mb-4">
  <!-- 缩略图 -->
  <img 
    src="/assets/images/spms-main-entrance.png" 
    alt="SPMS Main Entrance, NTU" 
    class="registration-img-thumbnail"
    data-bs-toggle="modal" 
    data-bs-target="#atriumImageModal"
  >
  <p class="mt-2 text-muted small text-center">Click the image to enlarge</p>
</div>

<!-- 图片放大模态框 -->
<div class="modal fade" id="atriumImageModal" tabindex="-1" aria-labelledby="atriumImageModalLabel" aria-hidden="true">
  <div class="modal-dialog modal-lg modal-dialog-centered">
    <div class="modal-content rounded-8 shadow-md">
      <div class="modal-header border-0 pb-0 px-4"> <!-- 增加水平内边距 -->
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body p-4"> <!-- 关键：将p-0改为p-4，给图片加内边距 -->
        <img src="/assets/images/spms-main-entrance.png" alt="SPMS Main Entrance, NTU" class="img-fluid rounded-6"> <!-- 图片单独加圆角 -->
      </div>
      <div class="modal-footer border-0 pt-2 pb-3 px-4"> <!-- 同步增加水平内边距 -->
        <span class="text-muted small">SPMS Main Entrance, NTU</span>
      </div>
    </div>
  </div>
</div>

<!-- 图片：缩略图+点击放大模态框 -->
<h3 class="h5 fw-medium text-dark mb-3">SPMS Atrium</h3>
<div class="registration-img-container mb-4">
  <!-- 缩略图 -->
  <img 
    src="/assets/images/location_atrium.png" 
    alt="SPMS Atrium, NTU" 
    class="registration-img-thumbnail"
    data-bs-toggle="modal" 
    data-bs-target="#atriumImageModal"
  >
  <p class="mt-2 text-muted small text-center">Click the image to enlarge</p>
</div>

<!-- 图片放大模态框 -->
<div class="modal fade" id="atriumImageModal" tabindex="-1" aria-labelledby="atriumImageModalLabel" aria-hidden="true">
  <div class="modal-dialog modal-lg modal-dialog-centered">
    <div class="modal-content rounded-8 shadow-md">
      <div class="modal-header border-0 pb-0 px-4"> <!-- 增加水平内边距 -->
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body p-4"> <!-- 关键：将p-0改为p-4，给图片加内边距 -->
        <img src="/assets/images/location_atrium.png" alt="SPMS Atrium, NTU" class="img-fluid rounded-6"> <!-- 图片单独加圆角 -->
      </div>
      <div class="modal-footer border-0 pt-2 pb-3 px-4"> <!-- 同步增加水平内边距 -->
        <span class="text-muted small">SPMS Atrium, NTU</span>
      </div>
    </div>
  </div>
</div>