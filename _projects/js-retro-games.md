---
title: "Js Retro Games"
tagline: "Classic retro games rebuilt to run on GitHub Pages."
description: >-
  Js Retro Games is a collection of remade retro games that run entirely in the
  browser on GitHub Pages — pick one up and play instantly, no download needed.
category: Game
tags: [free, game, retro, browser]
status: live              # live | beta | archived
live_url: https://jemmonsss.github.io/Js-Retro-Games/   # external live site (used for the iframe preview + "Live site" button)
repo: https://github.com/jemmonsss/Js-Retro-Games
featured: false
date: 2026-07-01
# `image` field intentionally omitted: the card shows a live <iframe> preview
# of the actual site (live_url) instead of a screenshot.
accent: "#a855f7"
layout: default
---

<article class="project-page">
  <h1>{{ page.title }}</h1>
  <p class="tagline">{{ page.tagline }}</p>

  Js Retro Games brings old-school classics back to life right in your browser.

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
