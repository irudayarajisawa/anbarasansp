---
layout: page
title:
permalink: /faculty
---

<!-- ================= TITLE ================= -->
<div class="section-title section-bg-img"
     style="background-image: url('/assets/img/profile/group.jpeg');">
    <h2>Members</h2>
    <div class="title-shape">
        <svg viewBox="0 0 200 20">
            <path d="M 0,10 C 40,0 60,20 100,10 C 140,0 160,20 200,10"
                  fill="none" stroke="currentColor" stroke-width="2"></path>
        </svg>
    </div>
</div>

<!-- ================= MAIN TABS ================= -->
<div class="faculty-tabs">
  <button class="tab-button active" data-tab="phd">Ph.D Students</button>
  <button class="tab-button" data-tab="msc">Master Students</button>
  <button class="tab-button" data-tab="parttime">Part Time</button>
  <button class="tab-button" data-tab="research">Research Associates</button>
  <button class="tab-button" data-tab="alumni">Alumni</button>
</div>

<!-- ================= Ph.D STUDENTS ================= -->
<div class="faculty-list" data-tab="phd">
{% for p in site.data.faculty.phd_students %}
  <div class="faculty-card">
    {% if p.image %}<img src="{{ p.image }}" alt="{{ p.name }}">{% endif %}
    <h3>{{ p.name }}</h3>
    {% if p.phd %}<p>{{ p.phd }}</p>{% endif %}
    {% if p.area_of_interest %}<p>{{ p.area_of_interest }}</p>{% endif %}
    {% if p.email and p.email != " " %}<p>✉️ <a href="mailto:{{ p.email }}">{{ p.email }}</a></p>{% endif %}
  </div>
{% endfor %}
</div>

<!-- ================= MASTER STUDENTS ================= -->
<div class="faculty-list" data-tab="msc" style="display:none;">
{% for p in site.data.faculty.master_students %}
  <div class="faculty-card">
    {% if p.image %}<img src="{{ p.image }}" alt="{{ p.name }}">{% endif %}
    <h3>{{ p.name }}</h3>
    {% if p.at_iitm %}<p>{{ p.at_iitm }}</p>{% endif %}
    {% if p.email and p.email != " " %}<p>✉️ <a href="mailto:{{ p.email }}">{{ p.email }}</a></p>{% endif %}
  </div>
{% endfor %}
</div>

<!-- ================= PART TIME ================= -->
<div class="faculty-list" data-tab="parttime" style="display:none;">
{% for p in site.data.faculty.part_time %}
  <div class="faculty-card">
    {% if p.image %}<img src="{{ p.image }}" alt="{{ p.name }}">{% endif %}
    <h3>{{ p.name }}</h3>
    {% if p.area_of_interest %}<p>{{ p.area_of_interest }}</p>{% endif %}
    {% if p.email and p.email != " " %}<p>✉️ <a href="mailto:{{ p.email }}">{{ p.email }}</a></p>{% endif %}
  </div>
{% endfor %}
</div>

<!-- ================= CURRENT RESEARCH ASSOCIATES ================= -->
<div class="faculty-list" data-tab="research" style="display:none;">
{% for p in site.data.faculty.research_associates.current %}
  <div class="faculty-card">
    {% if p.image %}<img src="{{ p.image }}" alt="{{ p.name }}">{% endif %}
    <h3>{{ p.name }}</h3>
    {% if p.at_iitm %}<p><strong>IITM:</strong> {{ p.at_iitm }}</p>{% endif %}
    {% if p.area_of_interest %}<p><strong>Research Area:</strong> {{ p.area_of_interest }}</p>{% endif %}
    {% if p.current_position and p.current_position != " " %}<p><strong>Current Position:</strong> {{ p.current_position }}</p>{% endif %}
    {% if p.email and p.email != " " %}<p>✉️ <a href="mailto:{{ p.email }}">{{ p.email }}</a></p>{% endif %}
    {% if p.contact %}<p>📞 {{ p.contact }}</p>{% endif %}
  </div>
{% endfor %}
</div>

<!-- ================= ALUMNI ================= -->
<div class="faculty-list alumni-section" data-tab="alumni" style="display:none;">
  <div class="faculty-tabs sub-tabs" style="width:100%; margin-bottom:20px;">
    <button class="tab-button active" data-group="phd">Ph.D</button>
    <button class="tab-button" data-group="msc">M.Sc</button>
    <button class="tab-button" data-group="research_associates">Research Associates</button>
  </div>

  <!-- ===== Ph.D ALUMNI ===== -->
  <div class="alumni-group" data-group="phd">
  {% for p in site.data.faculty.alumni.phd %}
    <div class="faculty-card">
      {% if p.image %}<img src="{{ p.image }}" alt="{{ p.name }}">{% endif %}
      <h3>{{ p.name }}</h3>
      {% if p.phd_year %}<p><strong>Ph.D:</strong> {{ p.phd_year }}</p>{% endif %}
      {% if p.thesis_title %}<p><em>{{ p.thesis_title }}</em></p>{% endif %}
      {% if p.current_position and p.current_position != " " %}<p>{{ p.current_position }}</p>{% endif %}
      {% if p.email and p.email != " " %}<p>✉️ <a href="mailto:{{ p.email }}">{{ p.email }}</a></p>{% endif %}
    </div>
  {% endfor %}
  </div>

  <!-- ===== M.Sc ALUMNI ===== -->
  <div class="alumni-group" data-group="msc" style="display:none;">
  {% for p in site.data.faculty.alumni.msc %}
    <div class="faculty-card">
      {% if p.image %}<img src="{{ p.image }}" alt="{{ p.name }}">{% endif %}
      <h3>{{ p.name }}</h3>
      {% if p.at_iitm %}<p>{{ p.at_iitm }}</p>{% endif %}
      {% if p.current_position and p.current_position != " " %}<p>{{ p.current_position }}</p>{% endif %}
      {% if p.email and p.email != " " %}<p>✉️ <a href="mailto:{{ p.email }}">{{ p.email }}</a></p>{% endif %}
    </div>
  {% endfor %}
  </div>

  <!-- ===== RESEARCH ASSOCIATE ALUMNI ===== -->
  <div class="alumni-group" data-group="research_associates" style="display:none;">
  {% for p in site.data.faculty.alumni.research_associates %}
    <div class="faculty-card">
      {% if p.image %}<img src="{{ p.image }}" alt="{{ p.name }}">{% endif %}
      <h3>{{ p.name }}</h3>
      {% if p.at_iitm %}<p><strong>IITM:</strong> {{ p.at_iitm }}</p>{% endif %}
      {% if p.area_of_interest %}<p><strong>Research Area:</strong> {{ p.area_of_interest }}</p>{% endif %}
      {% if p.current_position and p.current_position != " " %}<p><strong>Current Position:</strong> {{ p.current_position }}</p>{% endif %}
      {% if p.email and p.email != " " %}<p>✉️ <a href="mailto:{{ p.email }}">{{ p.email }}</a></p>{% endif %}
      {% if p.contact %}<p>📞 {{ p.contact }}</p>{% endif %}
    </div>
  {% endfor %}
  </div>
</div>

<!-- ================= SCRIPT ================= -->
<script>
/* MAIN TABS */
document.querySelectorAll('.faculty-tabs:not(.sub-tabs) > .tab-button').forEach(btn => {
  btn.addEventListener('click', () => {
    document.querySelectorAll('.faculty-tabs:not(.sub-tabs) > .tab-button')
      .forEach(b => b.classList.remove('active'));
    btn.classList.add('active');

    const tab = btn.dataset.tab;
    document.querySelectorAll('.faculty-list[data-tab]').forEach(section => {
      section.style.display = section.dataset.tab === tab ? 'flex' : 'none';
    });

    // Reset Alumni sub-tabs to Ph.D whenever Alumni is opened.
    if (tab === 'alumni') {
      document.querySelectorAll('.sub-tabs .tab-button')
        .forEach(b => b.classList.remove('active'));
      document.querySelector('.sub-tabs .tab-button[data-group="phd"]')
        .classList.add('active');

      document.querySelectorAll('.alumni-group').forEach(group => {
        group.style.display = group.dataset.group === 'phd' ? 'flex' : 'none';
      });
    }
  });
});

/* ALUMNI SUB TABS */
document.querySelectorAll('.sub-tabs .tab-button').forEach(btn => {
  btn.addEventListener('click', () => {
    document.querySelectorAll('.sub-tabs .tab-button')
      .forEach(b => b.classList.remove('active'));
    btn.classList.add('active');

    const group = btn.dataset.group;
    document.querySelectorAll('.alumni-group').forEach(section => {
      section.style.display = section.dataset.group === group ? 'flex' : 'none';
    });
  });
});
</script>

