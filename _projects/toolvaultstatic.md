---
title: "Toolvault Static"
tagline: "A lightweight, static version of the Toolsvault web tools."
description: >-
  Toolvault Static is the dependency-free, static-build companion to Toolsvault
  — the same handy browser tools, served as plain static pages for speed and
  portability.
category: Web App
tags: [free, tools, web, static]
status: live              # live | beta | archived
live_url: https://jemmonsss.github.io/toolvaultstatic/   # external live site (used for the iframe preview + "Live site" button)
repo: https://github.com/jemmonsss/toolvaultstatic
featured: false
date: 2026-07-11
# `image` field intentionally omitted: the card shows a live <iframe> preview
# of the actual site (live_url) instead of a screenshot.
accent: "#a855f7"
layout: default
---

<article class="project-page">
  <h1>{{ page.title }}</h1>
  <p class="tagline">{{ page.tagline }}</p>

  {{ content }}

  Toolvault Static delivers the same browser tools as a fast, static site you
  can host anywhere.

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
