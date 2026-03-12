---
layout: default
title: "Venue and Travel"
permalink: /venue/
---

<!-- 核心信息Hero区域（和首页风格统一） -->
<div class="hero mb-5">
  <div class="d-flex flex-column gap-3">
    <h1 class="display-5 fw-bold mb-2">Venue & Travel</h1>
    <p class="lead mb-0 opacity-90">
      How to get to NTU, Singapore
    </p>
  </div>
</div>

<!-- 核心场地信息卡片组（复用callout样式，和首页一致） -->
<div class="callouts my-5">
  <div class="callout">
    <h3>Workshop Venue</h3>
    <p class="mb-2">
      <strong>Nanyang Technological University (NTU)</strong>, Singapore
    </p>
    <p class="mb-1">
      Primary rooms: <a href="https://goo.gl/maps/mG3om1hxgET2" target="_blank" rel="noopener">The Hive</a> & <a href="https://goo.gl/maps/oPbRVcHvoun" target="_blank" rel="noopener">SPMS</a> (exact rooms TBC)
    </p>
    <p class="mb-0 text-muted small">
      NTU is located in Singapore’s west – well-connected by public transport/taxis
    </p>
  </div>

  <div class="callout">
    <h3>International Travel</h3>
    <p class="mb-1">
      Singapore’s main airport: <strong>Changi Airport (SIN)</strong>
    </p>
    <p class="mb-0">
      Extensive global flight connections with most countries
    </p>
  </div>

  <div class="callout">
    <h3>Getting to NTU</h3>
    <ul class="mb-0">
      <li class="mb-1"><strong>Taxi/Ride-hailing</strong>: Most convenient (door-to-door)</li>
      <li class="mb-1"><strong>Public Transport (MRT + Bus)</strong>:
        <ul class="mb-0 mt-1 text-muted">
          <li>~1 hour from Changi Airport → City Centre</li>
          <li>~1 hour from City Centre → NTU</li>
        </ul>
      </li>
    </ul>
  </div>

  <div class="callout">
    <h3>Nearby Events</h3>
    <ul class="mb-0">
      <li class="mb-1">Spring School on Symmetric Cryptography: 16–18 March 2026</li>
      <li class="mb-0"><a href="https://fse.iacr.org/2026/" target="_blank" rel="noopener">FSE/ToSC 2026</a>: 23–27 March 2026 (Parkroyal Hotel on Beach Road)</li>
    </ul>
  </div>
</div>

<!-- EWL停运警示框（浅橙/黄，支持图片放大） -->
<div class="alert alert-warning my-5" role="alert">
  <h2 class="h4 mb-3 fw-semibold">No East-West Line (EWL) train services between Tanah Merah (CG) and Expo (CG1) from Mar 14 to 17, 2026</h2>
  <p class="mb-3">
    Train services along the East-West Line (EWL) and Sengkang-Punggol LRT (SPLRT) will be adjusted to facilitate essential upgrading works that will enhance the capacity, reliability and resilience of the rail network. (<a href="https://www.lta.gov.sg/content/ltagov/en/newsroom/2026/2/news-releases/train-service-adjustment-ewl-splrt-upgrading-works.html" target="_blank" rel="noopener">LTA Train Service Adjustment (EWL/SPLRT) 2026</a>)
  </p>
  <p class="mb-3">
    During this period, commuters are advised to take the <strong>Shuttle Bus Service S8</strong> or other alternatives.
  </p>
  <p class="mb-2 fw-medium">Service adjustment info from LTA website (click to enlarge):</p>
  <br/>

  <div class="row g-3 mb-4">
    <!-- 第一张图片 -->
    <div class="col-md-6 d-flex justify-content-center">
      <img 
        src="/assets/images/ewl_adjustment_route.png" 
        alt="EWL 2026 Service Adjustment Map - Route" 
        class="img-fluid rounded shadow-sm" 
        style="cursor: zoom-in; max-width: 90%;"
        data-bs-toggle="modal" 
        data-bs-target="#ewlMapModal1"
      >
    </div>
    <!-- 第二张图片 -->
    <div class="col-md-6 d-flex justify-content-center">
      <img 
        src="/assets/images/ewl_adjustment_shuttle_bus.png"
        alt="EWL 2026 Service Adjustment - Shuttle Bus" 
        class="img-fluid rounded shadow-sm" 
        style="cursor: zoom-in; max-width: 72%;"
        data-bs-toggle="modal" 
        data-bs-target="#ewlMapModal2"
      >
    </div>
  </div>
</div>

<!-- 提示框（复用alert样式，和首页一致） -->
<div class="alert alert-info my-5" role="alert">
  <h2 class="h4 mb-3 fw-semibold">Travel Updates</h2>
  <p class="mb-0">
    Practical travel tips, campus directions, and local transit hacks will be posted here closer to the event.
    For urgent questions, reach out via the <a href="{{ '/contact/' | relative_url }}" style="color: var(--primary-color); font-weight: 500;">contact page</a>.
  </p>
</div>

<!-- 第一张图片的放大模态框 -->
<div class="modal fade" id="ewlMapModal1" tabindex="-1" aria-labelledby="ewlMapModal1Label" aria-hidden="true">
  <div class="modal-dialog modal-xl">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="ewlMapModal1Label">EWL 2026 Service Adjustment Map - Affected Route</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body p-0">
        <img src="/assets/images/ewl_adjustment_route.png" alt="EWL 2026 Service Adjustment Map" class="img-fluid w-100">
      </div>
    </div>
  </div>
</div>

<!-- 第二张图片的放大模态框 -->
<div class="modal fade" id="ewlMapModal2" tabindex="-1" aria-labelledby="ewlMapModal2Label" aria-hidden="true">
  <div class="modal-dialog modal-xl">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="ewlMapModal2Label">EWL 2026 Service Adjustment - Shuttle Bus</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body p-0">
        <img src="/assets/images/ewl_adjustment_shuttle_bus.png" alt="Shuttle Bus es" class="img-fluid w-100">
      </div>
    </div>
  </div>
</div>