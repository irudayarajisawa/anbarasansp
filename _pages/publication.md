---
layout: default
title: Publications
permalink: /publication
---

<!-- ==========================================
     PAGE HEADER
========================================== -->

<div class="container">
  <div class="section-title section-bg-img"
       style="background-image: url('/assets/img/profile/publications.jpeg');">

    <h2>Publications</h2>

    <div class="title-shape">
      <svg viewBox="0 0 200 20">
        <path d="M 0,10 C 40,0 60,20 100,10 C 140,0 160,20 200,10"
              fill="none"
              stroke="currentColor"
              stroke-width="2"></path>
      </svg>
    </div>

  </div>
</div>


<!-- ==========================================
     PUBLICATION CONTAINER
========================================== -->

<div class="container publication-container">

  <!-- CATEGORY BUTTONS -->

  <div class="pub-btn-group">

    <button type="button"
            class="pub-btn active"
            onclick="showSection('iitm', this)">
      IITM
    </button>

    <button type="button"
            class="pub-btn"
            onclick="showSection('phd', this)">
      PhD &amp; Postdoc
    </button>

    <button type="button"
            class="pub-btn"
            onclick="showSection('review', this)">
      Reviews
    </button>

    <button type="button"
            class="pub-btn"
            onclick="showSection('bookchapter', this)">
      Book Chapters
    </button>

    <button type="button"
            class="pub-btn"
            onclick="showSection('patent', this)">
      Patents
    </button>

    <button type="button"
            class="pub-btn"
            onclick="showSection('highlight', this)">
      Highlights
    </button>

  </div>


  <!-- ==========================================
       YEAR FILTER AND SEARCH
  ========================================== -->

  <div class="pub-filter-bar">

    <div class="pub-filter-left">

      <select id="yearFilter"
              aria-label="Filter publications by year"
              onchange="filterPublications()">

        <option value="all">Filter by Year</option>

        {% assign publication_years = "2026,2025,2024,2023,2022,2021,2020,2019,2018,2017,2016,2015,2014,2013,2012,2011,2010,2009,2008,2007,2006,2005" | split: "," %}

        {% for year in publication_years %}
          <option value="{{ year }}">{{ year }}</option>
        {% endfor %}

      </select>

    </div>

    <div class="pub-filter-right">

      <input
        type="text"
        id="searchInput"
        placeholder="Search publications..."
        aria-label="Search publications"
        oninput="filterPublications()">

    </div>

  </div>


  <!-- ==========================================
       IITM PUBLICATIONS
  ========================================== -->

  <div id="section-iitm"
       class="pub-section active-section">

    <h3>IITM</h3>

    <ul class="pub-list">

      {% for item in site.data.publications.iitm %}

        <li class="publication-item"
            data-year="{% assign pub_year = item.text | strip_html | remove: '<b>' | remove: '</b>' | split: ' ' %}{% assign found_year = '' %}{% for word in pub_year %}{% assign clean_word = word | remove: ',' | remove: '.' | remove: ';' %}{% if clean_word.size == 4 and clean_word contains '20' %}{% assign found_year = clean_word %}{% endif %}{% endfor %}{{ found_year }}">

          <!-- PUBLICATION NUMBER -->

          <div class="pub-number">
            {{ item.number }}
          </div>


          <!-- JOURNAL COVER -->

          <div class="pub-cover">

            {% if item.cover %}

              <img
                src="{{ item.cover | relative_url }}"
                alt="Journal cover for publication {{ item.number }}"
                loading="lazy">

            {% else %}

              <div class="pub-cover-placeholder">
                <span>Journal cover unavailable</span>
              </div>

            {% endif %}

          </div>

          <!-- PUBLICATION DETAILS: title bold, remaining citation normal -->
          <div class="pub-details">

    <div class="pub-text">
  {{ item.text }}
  
  {% if item.link %}
    <a class="pub-view-link"
       href="{{ item.link | strip }}"
       target="_blank"
       rel="noopener noreferrer">[Click Here]</a>
  {% endif %}
</div>

</div>


          <!-- GRAPHICAL ABSTRACT -->

          {% if item.image %}

            <div class="pub-graphical-abstract">

              <a href="{{ item.image | relative_url }}"
                 target="_blank"
                 rel="noopener noreferrer"
                 aria-label="View graphical abstract for publication {{ item.number }}">

                <img
                  src="{{ item.image | relative_url }}"
                  alt="Graphical abstract for publication {{ item.number }}"
                  loading="lazy">

              </a>

            </div>

          {% endif %}

        </li>

      {% endfor %}

    </ul>

  </div>


  <!-- ==========================================
       PHD AND POSTDOC
  ========================================== -->

  <div id="section-phd" class="pub-section">

    <h3>PhD &amp; Postdoc</h3>

    <ul class="pub-list">

      {% for item in site.data.publications.phd %}

        <li class="pub-legacy-item">

          <div class="pub-text-line">

            <span class="pub-no">
              {{ item.number }}.
            </span>

            <span class="pub-text">

              {{ item.text }}

              {% if item.link %}

                <a href="{{ item.link | strip }}"
                   target="_blank"
                   rel="noopener noreferrer">
                  [Click Here]
                </a>

              {% endif %}

            </span>

          </div>

        </li>

      {% endfor %}

    </ul>

  </div>


  <!-- ==========================================
       REVIEWS
  ========================================== -->

  <div id="section-review" class="pub-section">

    <h3>Reviews</h3>

    <ul class="pub-list">

      {% for item in site.data.publications.review %}

        <li class="pub-legacy-item">

          <div class="pub-text-line">

            <span class="pub-no">
              {{ item.number }}.
            </span>

            <span class="pub-text">

              {{ item.text }}

              {% if item.link %}

                <a href="{{ item.link | strip }}"
                   target="_blank"
                   rel="noopener noreferrer">
                  [Click Here]
                </a>

              {% endif %}

            </span>

          </div>

          {% if item.image %}

            <div class="pub-image-block">

              <img
                src="{{ item.image | relative_url }}"
                alt="Graphical abstract for review {{ item.number }}"
                loading="lazy">

            </div>

          {% endif %}

        </li>

      {% endfor %}

    </ul>

  </div>


  <!-- ==========================================
       BOOK CHAPTERS
  ========================================== -->

  <div id="section-bookchapter" class="pub-section">

    <h3>Book Chapters</h3>

    <ul class="pub-list">

      {% for item in site.data.publications.book_chapter %}

        <li class="pub-legacy-item">

          <div class="pub-text-line">

            <span class="pub-no">
              {{ item.number }}.
            </span>

            <span class="pub-text">

              {{ item.text }}

              {% if item.link %}

                <a href="{{ item.link | strip }}"
                   target="_blank"
                   rel="noopener noreferrer">
                  [Click Here]
                </a>

              {% endif %}

            </span>

          </div>

        </li>

      {% endfor %}

    </ul>

  </div>


  <!-- ==========================================
       PATENTS
  ========================================== -->

  <div id="section-patent" class="pub-section">

    <h3>Patents</h3>

    <ul class="pub-list">

      {% for item in site.data.publications.patent %}

        <li class="pub-legacy-item">

          <div class="pub-text-line">

            <span class="pub-no">
              {{ item.number }}.
            </span>

            <span class="pub-text">

              {{ item.text }}

              {% if item.link %}

                <a href="{{ item.link | strip }}"
                   target="_blank"
                   rel="noopener noreferrer">
                  [Click Here]
                </a>

              {% endif %}

            </span>

          </div>

        </li>

      {% endfor %}

    </ul>

  </div>


  <!-- ==========================================
       HIGHLIGHTS
  ========================================== -->

  <div id="section-highlight" class="pub-section">

    <h3>Highlights</h3>

    <ul class="pub-list">

      {% for item in site.data.publications.highlights %}

        <li class="pub-legacy-item">

          <div class="pub-text-line">

            <span class="pub-no">
              {{ item.number }}.
            </span>

            <span class="pub-text">

              {{ item.text }}

              {% if item.link %}

                <a href="{{ item.link | strip }}"
                   target="_blank"
                   rel="noopener noreferrer">
                  [Click Here]
                </a>

              {% endif %}

              {% if item.links %}

                <div class="pub-extra-links">

                  {% for l in item.links %}

                    <div>
                      <a href="{{ l.url }}"
                         target="_blank"
                         rel="noopener noreferrer">
                        {{ l.label }}
                      </a>
                    </div>

                  {% endfor %}

                </div>

              {% endif %}

            </span>

          </div>

          {% if item.image %}

            <div class="pub-image-block highlight-img">

              <img
                src="{{ item.image | relative_url }}"
                alt="Publication highlight {{ item.number }}"
                loading="lazy">

            </div>

          {% endif %}

        </li>

      {% endfor %}

    </ul>

  </div>

</div>


<!-- ==========================================
     PUBLICATION CITATION FORMATTING
     Keeps the JSON structure unchanged.
========================================== -->
<style>
  #section-iitm .pub-text {
    font-size: 16px;
    line-height: 1.7;
    font-weight: 400;
    color: #111;
    overflow-wrap: anywhere;
  }

  #section-iitm .pub-citation-text strong,
  #section-iitm .pub-citation-text b {
    font-weight: 400;
  }

  #section-iitm .pub-inline-link {
    display: inline;
    margin-left: 6px;
    color: #0077b6;
    font-size: inherit;
    font-weight: 400;
    text-decoration: none;
    white-space: nowrap;
  }

  #section-iitm .pub-inline-link:hover {
    text-decoration: underline;
  }
</style>


<!-- ==========================================
     JAVASCRIPT
========================================== -->

<script>
(function () {

  let currentSectionId = 'section-iitm';

  /*
   * Show selected publication category.
   */
  window.showSection = function (section, btn) {

    document.querySelectorAll('.pub-section').forEach(function (element) {
      element.classList.remove('active-section');
    });

    document.querySelectorAll('.pub-btn').forEach(function (button) {
      button.classList.remove('active');
    });

    currentSectionId = 'section-' + section;

    const activeSection = document.getElementById(currentSectionId);

    if (!activeSection) return;

    activeSection.classList.add('active-section');

    if (btn) {
      btn.classList.add('active');
    }

    document.getElementById('yearFilter').value = 'all';
    document.getElementById('searchInput').value = '';

    filterPublications();

  };


  /*
   * Bold only the publication title while leaving the rest of item.text
   * (authors, journal, year, volume and pages) in normal font weight.
   * JSON remains unchanged. This expects the title to end at the first
   * period followed by a space.
   */
  function formatPublicationCitations() {
    document.querySelectorAll('#section-iitm .pub-citation-text').forEach(function (element) {
      if (element.dataset.formatted === 'true') return;

      const originalHtml = element.innerHTML.trim();
      const match = originalHtml.match(/^([\s\S]*?\.)\s+([\s\S]*)$/);

      if (match) {
        element.innerHTML = '<strong>' + match[1] + '</strong> ' + match[2];
      }

      element.dataset.formatted = 'true';
    });
  }


  /*
   * Determine publication year.
   */
  function extractYear(text) {

    const matches = text.match(/\b(?:19|20)\d{2}\b/g);

    if (!matches || matches.length === 0) {
      return '';
    }

    /*
     * The last year in a citation is usually the publication year.
     */
    return matches[matches.length - 1];

  }


  /*
   * Assign a year to every publication.
   */
  function attachYears() {

    document.querySelectorAll('.pub-list > li').forEach(function (item) {

      const textElement = item.querySelector('.pub-title, .pub-text');

      const text = textElement
        ? textElement.textContent
        : item.textContent;

      item.dataset.year = extractYear(text);

    });

  }


  /*
   * Filter the active category by year and search text.
   */
  window.filterPublications = function () {

    const yearFilter = document.getElementById('yearFilter');
    const searchInput = document.getElementById('searchInput');

    if (!yearFilter || !searchInput) return;

    const selectedYear = yearFilter.value;
    const searchText = searchInput.value.trim().toLowerCase();

    const activeSection = document.getElementById(currentSectionId);

    if (!activeSection) return;

    activeSection.querySelectorAll('.pub-list > li').forEach(function (item) {

      const itemYear = item.dataset.year || '';

      const itemText = item.textContent.toLowerCase();

      const matchesYear =
        selectedYear === 'all' || itemYear === selectedYear;

      const matchesSearch =
        itemText.includes(searchText);

      /*
       * Restore the original CSS display mode.
       * Do not force grid publication rows to display:block.
       */
      item.style.display =
        matchesYear && matchesSearch ? '' : 'none';

    });

  };


  /*
   * Initialise the page.
   */
  document.addEventListener('DOMContentLoaded', function () {

    formatPublicationCitations();
    attachYears();

    const defaultButton = document.querySelector(
      '.pub-btn[onclick*="showSection(\'iitm\'"]'
    );

    window.showSection('iitm', defaultButton);

  });

})();
</script>
