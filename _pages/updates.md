---
title: null
layout: page
permalink: "/updates"
---

<div class="section-title">
  <h2>Updates</h2>

  <div class="title-shape">
    <svg viewBox="0 0 200 20" xmlns="http://www.w3.org/2000/svg">
      <path
        d="M 0,10 C 40,0 60,20 100,10 C 140,0 160,20 200,10"
        fill="none"
        stroke="currentColor"
        stroke-width="2">
      </path>
    </svg>
  </div>
</div>

<h3 class="mt-4 mb-3" style="color:#5e1f1f;">
  Latest Updates
</h3>

<div class="container my-4">
  <div class="row">

    {% assign half = site.data.latestupdates.size | divided_by: 2 %}

    <div class="col-md-6">
      <ul>
        {% for update in site.data.latestupdates limit:half %}
        <li class="mb-3">
          {{ update.text }}
        </li>
        {% endfor %}
      </ul>
    </div>

    <div class="col-md-6">
      <ul>
        {% for update in site.data.latestupdates offset:half %}
        <li class="mb-3">
          {{ update.text }}
        </li>
        {% endfor %}
      </ul>
    </div>

  </div>
</div>
