---
layout: default
title: 
permalink: /publication
---

<div class="container">
  <div class="section-title section-bg-img" 
       style="background-image: url('/anbarasansp/assets/img/profile/publications.jpeg');">

    <h2>Publications</h2>

    <div class="title-shape">
      <svg viewBox="0 0 200 20">
        <path d="M 0,10 C 40,0 60,20 100,10 C 140,0 160,20 200,10"
              fill="none" stroke="currentColor" stroke-width="2"></path>
      </svg>
    </div>

  </div>
</div>

<!-- CONTENT INSIDE CONTAINER -->
<div class="container publication-container">

<!-- ===== BUTTONS (IITM FIRST & ACTIVE) ===== -->
<div class="pub-btn-group">
  <button class="pub-btn active" onclick="showSection('iitm', this)">IITM</button>
  <button class="pub-btn" onclick="showSection('phd', this)">PhD & Postdoc</button>
  <button class="pub-btn" onclick="showSection('review', this)">Reviews</button>
  <button class="pub-btn" onclick="showSection('bookchapter', this)">Book Chapters</button>
  <button class="pub-btn" onclick="showSection('patent', this)">Patents</button>
  <button class="pub-btn" onclick="showSection('highlight', this)">Highlights</button>
</div>

<!-- ===== FILTER BAR ===== -->
<div class="pub-filter-bar">
  <!-- LEFT: YEAR FILTER -->
  <div class="pub-filter-left">
    <select id="yearFilter" onchange="filterPublications()">
      <option value="all">Filter by Year</option>
      <option value="2025">2025</option>
      <option value="2024">2024</option>
      <option value="2023">2023</option>
      <option value="2022">2022</option>
      <option value="2021">2021</option>
      <option value="2020">2020</option>
      <option value="2019">2019</option>
      <option value="2018">2018</option>
      <option value="2017">2017</option>
      <option value="2016">2016</option>
      <option value="2015">2015</option>
      <option value="2014">2014</option>
      <option value="2013">2013</option>
      <option value="2012">2012</option>
      <option value="2011">2011</option>
      <option value="2010">2010</option>
    </select>
  </div>

  <!-- RIGHT: SEARCH -->
  <div class="pub-filter-right">
    <input
      type="text"
      id="searchInput"
      placeholder="Search publications..."
      onkeyup="filterPublications()"
    >
  </div>
</div>



<!-- ===== SECTIONS ===== -->

<!-- IITM (DEFAULT VISIBLE) -->
<div id="section-iitm" class="pub-section">
  <h3>IITM</h3>

  <ul class="pub-list">
    {% for item in site.data.publications.iitm %}
      <li style="margin-bottom:24px;">
        <div class="pub-text-line">
          <span class="pub-no">{{ item.number }}.</span>
          <span class="pub-text">
            {{ item.text }}
            {% if item.link %}
              <a href="{{ item.link }}" target="_blank">[Click Here]</a>
            {% endif %}
          </span>
        </div>

        {% if item.image %}
          <div class="pub-image-block">
            <img src="{{ item.image }}" alt="reaction scheme">
          </div>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</div>

<!-- PhD & Postdoc -->
<div id="section-phd" class="pub-section" style="display:none;">
  <h3>PhD & Postdoc</h3>

  <ul class="pub-list">
    {% for item in site.data.publications.phd %}
      <li style="margin-bottom:24px;">
        <div class="pub-text-line">
          <span class="pub-no">{{ item.number }}.</span>
          <span class="pub-text">
            {{ item.text }}
            {% if item.link %}
              <a href="{{ item.link }}" target="_blank">[Click Here]</a>
            {% endif %}
          </span>
        </div>
      </li>
    {% endfor %}
  </ul>
</div>

<!-- Reviews -->
<div id="section-review" class="pub-section" style="display:none;">
  <h3>Reviews</h3>

  <ul class="pub-list">
    {% for item in site.data.publications.review %}
      <li style="margin-bottom:24px;">
        <div class="pub-text-line">
          <span class="pub-no">{{ item.number }}.</span>
          <span class="pub-text">
            {{ item.text }}
            {% if item.link %}
              <a href="{{ item.link }}" target="_blank">[Click Here]</a>
            {% endif %}
          </span>
        </div>

        {% if item.image %}
          <div class="pub-image-block">
            <img src="{{ item.image }}" alt="reaction scheme">
          </div>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</div>

<!-- Book Chapters -->
<div id="section-bookchapter" class="pub-section" style="display:none;">
  <h3>Book Chapters</h3>

  <ul class="pub-list">
    {% for item in site.data.publications.book_chapter %}
      <li style="margin-bottom:24px;">
        <div class="pub-text-line">
          <span class="pub-no">{{ item.number }}.</span>
          <span class="pub-text">
            {{ item.text }}
            {% if item.link %}
              <a href="{{ item.link }}" target="_blank">[Click Here]</a>
            {% endif %}
          </span>
        </div>
      </li>
    {% endfor %}
  </ul>
</div>

<!-- Patents -->
<div id="section-patent" class="pub-section" style="display:none;">
  <h3>Patents</h3>

  <ul class="pub-list">
    {% for item in site.data.publications.patent %}
      <li style="margin-bottom:24px;">
        <div class="pub-text-line">
          <span class="pub-no">{{ item.number }}.</span>
          <span class="pub-text">
            {{ item.text }}
            {% if item.link %}
              <a href="{{ item.link }}" target="_blank">[Click Here]</a>
            {% endif %}
          </span>
        </div>
      </li>
    {% endfor %}
  </ul>
</div>

<!-- Highlights -->
<div id="section-highlight" class="pub-section" style="display:none;">
  <h3>Highlights</h3>

  <ul class="pub-list">
    {% for item in site.data.publications.highlights %}
      <li style="margin-bottom:24px;">
        <div class="pub-text-line">
          <span class="pub-no">{{ item.number }}.</span>

          <span class="pub-text">
            {{ item.text }}

            {% if item.link %}
              <a href="{{ item.link }}" target="_blank">[Click Here]</a>
            {% endif %}

            {% if item.links %}
              <div class="pub-extra-links">
                {% for l in item.links %}
                  <div>
                    <a href="{{ l.url }}" target="_blank">{{ l.label }}</a>
                  </div>
                {% endfor %}
              </div>
            {% endif %}
          </span>
        </div>

        {% if item.image %}
          <div class="pub-image-block highlight-img">
            <img src="{{ item.image }}" alt="Journal cover image">
          </div>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</div>

</div>

<!-- ===== JS ===== -->
<script>
let currentSectionId = 'section-iitm'; // default

function showSection(section, btn) {
  // hide all sections
  document.querySelectorAll('.pub-section').forEach(s => s.style.display = 'none');
  document.querySelectorAll('.pub-btn').forEach(b => b.classList.remove('active'));

  // show selected section
  currentSectionId = 'section-' + section;
  const activeSection = document.getElementById(currentSectionId);
  activeSection.style.display = 'block';
  btn.classList.add('active');

  // reset filters for new section
  document.getElementById('yearFilter').value = 'all';
  document.getElementById('searchInput').value = '';

  filterPublications();
}

function extractYear(text) {
  const match = text.match(/\b(20\d{2})\b/);
  return match ? match[1] : 'unknown';
}

function attachYears() {
  document.querySelectorAll('.pub-list li').forEach(li => {
    li.dataset.year = extractYear(li.innerText);
  });
}

function filterPublications() {
  const year = document.getElementById('yearFilter').value;
  const search = document.getElementById('searchInput').value.toLowerCase();

  const activeSection = document.getElementById(currentSectionId);
  if (!activeSection) return;

  const items = activeSection.querySelectorAll('li');

  items.forEach(item => {
    const itemYear = item.dataset.year;
    const text = item.innerText.toLowerCase();

    const yearMatch = (year === 'all' || itemYear === year);
    const searchMatch = text.includes(search);

    item.style.display = (yearMatch && searchMatch) ? 'block' : 'none';
  });
}

document.addEventListener('DOMContentLoaded', function () {
  attachYears();
  document.querySelector('.pub-btn.active')?.click();
});
</script>





