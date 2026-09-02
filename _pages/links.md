---
layout: page
title:
permalink: /links
---
<!-- =========================
  PAGE TITLE
========================= -->
<div class="section-title section-bg-img" style="background-image: url('{{ site.baseurl }}/assets/img/profile/linksbg.jpeg');">
    <h2>Links</h2>

    <div class="title-shape">
        <svg viewBox="0 0 200 20">
            <path d="M 0,10 C 40,0 60,20 100,10 C 140,0 160,20 200,10"
                  fill="none" stroke="currentColor" stroke-width="2"></path>
        </svg>
    </div>
</div>

{% assign tables = site.data.links.tables %}

<div class="container my-5">
  <div class="row justify-content-center g-4">

    <!-- LEFT CARD -->
    <div class="col-md-5">
      <div class="link-card">
        {% for section in tables[0].sections %}
        <div class="link-section">
          <h5 class="link-title">{{ section.title }}</h5>
          <ul class="link-list">
            {% for item in section.links %}
            <li>
              <a href="https://{{ item.url }}" target="_blank"
   class="{% if item.highlight %}highlight-link{% endif %}">
  {{ item.name }}
</a>
            </li>
            {% endfor %}
          </ul>
        </div>
        {% endfor %}
      </div>
    </div>

    <!-- RIGHT CARD -->
    <div class="col-md-5">
      <div class="link-card">
        <h5 class="link-title">Other Useful Links</h5>
        <ul class="link-list">
          {% for item in tables[1].sections[0].links %}
          <li>
            <a href="https://{{ item.url }}" target="_blank">
              {{ item.name }}
            </a>
          </li>
          {% endfor %}
        </ul>
      </div>
    </div>

  </div>
</div>






