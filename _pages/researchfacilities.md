---
title: null
layout: page
permalink: "/researchfacilities"
---

<!-- =========================
  PAGE TITLE
========================= -->
<div class="section-title section-bg-img"
     style="background-image: url('{{ site.baseurl }}/assets/img/profile/instruments.jpeg');">
    <h2>Research Facilities</h2>

    <div class="title-shape">
        <svg viewBox="0 0 200 20">
            <path d="M 0,10 C 40,0 60,20 100,10 C 140,0 160,20 200,10"
                  fill="none" stroke="currentColor" stroke-width="2"></path>
        </svg>
    </div>
</div>

<style>
/* ===== GRID LAYOUT ===== */
.instrument-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 20px;
  margin-top: 20px;
}

/* ===== CARD ===== */
.instrument-card {
  background: #fff;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 4px 15px rgba(0,0,0,0.08);
  transition: 0.3s ease;
}

.instrument-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 25px rgba(0,0,0,0.15);
}

/* ===== IMAGE ===== */
.instrument-card img {
  width: 100%;
  height: 300px;
  object-fit: cover;
}

/* ===== TEXT ===== */
.instrument-info {
  padding: 12px 15px;
  text-align: center;
}

.instrument-info h4 {
  font-size: 16px;
  margin: 0;
  color: #000000;
  font-weight: 700 !important;
}

.instrument-info p {
  font-size: 13px;
  color: #777;
  margin-top: 5px;
}
</style>

<div class="instrument-grid">

  <!-- CARD 1 -->
  <div class="instrument-card">
    <img src="{{ site.baseurl }}/assets/img/instruments/chiralhplc.jpeg">
    <div class="instrument-info">
      <h4>Chiral HPLC</h4>
    </div>
  </div>

  <!-- CARD 2 -->
  <div class="instrument-card">
    <img src="{{ site.baseurl }}/assets/img/instruments/cryogenic.jpeg">
    <div class="instrument-info">
      <h4>Cryogenic reactionbath</h4>     
    </div>
  </div>

  <!-- CARD 3 -->
  <div class="instrument-card">
    <img src="{{ site.baseurl }}/assets/img/instruments/flashchromatography.jpeg">
    <div class="instrument-info">
      <h4>Flash Chromatography</h4>     
    </div>
  </div>

  <!-- CARD 4 -->
  <div class="instrument-card">
    <img src="{{ site.baseurl }}/assets/img/instruments/gcms.jpeg">
    <div class="instrument-info">
      <h4>GC-MS</h4>     
    </div>
  </div>

  <!-- CARD 5 -->
  <div class="instrument-card">
    <img src="{{ site.baseurl }}/assets/img/instruments/glovebox.jpeg">
    <div class="instrument-info">
      <h4>Glove Box</h4>    
    </div>
  </div>

  <!-- CARD 6 -->
  <div class="instrument-card">
    <img src="{{ site.baseurl }}/assets/img/instruments/hplc.jpeg">
    <div class="instrument-info">
      <h4>HPLC</h4>
    </div>
  </div>
  
  <!-- CARD 7 -->
  <div class="instrument-card">
    <img src="{{ site.baseurl }}/assets/img/instruments/uvphotoreactor.jpeg">
    <div class="instrument-info">
      <h4>UV photoreactor</h4>    
    </div>
  </div>
  
  <!-- CARD 8 -->
  <div class="instrument-card">
    <img src="{{ site.baseurl }}/assets/img/instruments/mercurylamp.jpeg">
    <div class="instrument-info">
      <h4>Mercury lamp photoreactor</h4>    
    </div>
  </div>
  
  <!-- CARD 9 -->
  <div class="instrument-card">
    <img src="{{ site.baseurl }}/assets/img/instruments/visiblelight.jpeg">
    <div class="instrument-info">
      <h4>Visible light photoreactor</h4>    
    </div>
  </div>
  
  <!-- CARD 10 -->
  <div class="instrument-card">
    <img src="{{ site.baseurl }}/assets/img/instruments/parallel.jpeg">
    <div class="instrument-info">
      <h4>Parallel synthesizer</h4>    
    </div>
  </div>
  
  <!-- CARD 11 -->
  <div class="instrument-card">
    <img src="{{ site.baseurl }}/assets/img/instruments/parrreactor.jpeg">
    <div class="instrument-info">
      <h4>Parr reactor</h4>    
    </div>
  </div>
  
  <!-- CARD 12 -->
  <div class="instrument-card">
    <img src="{{ site.baseurl }}/assets/img/instruments/weighingbalance.jpeg">
    <div class="instrument-info">
      <h4>Weighing balance</h4>    
    </div>
  </div>
  
  <!-- CARD 13 -->
  <div class="instrument-card">
    <img src="{{ site.baseurl }}/assets/img/instruments/rotaryevaporator.jpeg">
    <div class="instrument-info">
      <h4>Rotary evaporator</h4>    
    </div>
  </div>
  
  <!-- CARD 14 -->
  <div class="instrument-card">
    <img src="{{ site.baseurl }}/assets/img/instruments/immersioncooler.jpeg">
    <div class="instrument-info">
      <h4>Immersion Cooler</h4>    
    </div>
  </div>
	

  

</div>
