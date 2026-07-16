---
title: "Meta Data Editor"
tagline: "A free, browser-based metadata editor."
description: >-
  Js Meta Data Editor is a free web tool for viewing and editing file metadata
  directly in the browser — quick, simple, and client-side.
category: Tool
tags: [free, tool, metadata, editor]
status: live              # live | beta | archived
live_url: https://jemmonsss.github.io/Js-Meta-Data-Editor/   # external live site (used for the iframe preview + "Live site" button)
repo: https://github.com/jemmonsss/Js-Meta-Data-Editor
featured: false
date: 2025-11-19
# `image` field intentionally omitted: the card shows a live <iframe> preview
# of the actual site (live_url) instead of a screenshot.
accent: "#a855f7"
layout: default
---

<article class="project-page">
  <h1>{{ page.title }}</h1>
  <p class="tagline">{{ page.tagline }}</p>

  {{ content }}

  Tweak and inspect metadata without installing anything — just open the page.

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
