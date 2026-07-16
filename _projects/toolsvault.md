---
title: "Toolsvault"
tagline: "A growing collection of free, browser-based web tools."
description: >-
  Toolsvault is a free, public hub of small web utilities — converters,
  generators, and helpers — all running client-side in the browser.
category: Web App
tags: [free, tools, web, utilities]
status: live              # live | beta | archived
live_url: https://toolsvault.org/   # external live site (custom domain; used for the iframe preview + "Live site" button)
repo: https://github.com/jemmonsss/toolsvault
featured: true
date: 2026-07-12
# `image` field intentionally omitted: the card shows a live <iframe> preview
# of the actual site (live_url) instead of a screenshot.
accent: "#a855f7"
layout: default
---

<article class="project-page">
  <h1>{{ page.title }}</h1>
  <p class="tagline">{{ page.tagline }}</p>

  {{ content }}

  Toolsvault bundles a library of handy browser tools in one place — no
  installs, no accounts, just open and use.

  <div class="links">
    {% if page.live_url and page.live_url != empty %}
      <a class="btn btn-primary" href="{{ page.live_url }}" target="_blank" rel="noopener">Live site</a>
    {% endif %}
    {% if page.repo %}
      <a class="btn" href="{{ page.repo }}" target="_blank" rel="noopener">Source</a>
    {% endif %}
  </div>

  {% if page.tags %}
    <p style="margin-top:1.5rem">
      {% for tag in page.tags %}<span class="tag-pill">{{ tag }}</span>{% endfor %}
    </p>
  {% endif %}
</article>
