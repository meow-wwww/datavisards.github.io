---
layout: page
title: Logo
permalink: /logo/
class: logo
description: The VisArds logo — a wand from VIS and HCI, a sorting-hat A in the Hogwarts house colors, merging into black.
---

{% assign logo = site.data.logo %}

<h1 class="visually-hidden">Logo</h1>

<p class="lead">Check our logo!</p>

<div class="logo-explorer" data-logo-explorer>
  <div class="logo-stage">
    {% include logo-mark.svg %}
  </div>

  <p class="logo-hint">{{ logo.hint }}</p>

  <div class="logo-story">
    {% for part in logo.parts %}
    <button type="button" class="logo-story-card" data-part="{{ part.id }}" aria-pressed="false">
      <span class="logo-story-label">{{ part.label }}</span>
      <span class="logo-story-copy">{{ part.html }}</span>
    </button>
    {% endfor %}
  </div>
</div>
