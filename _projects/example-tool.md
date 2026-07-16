---
title: "Knolagebase"
tagline: "A free knowledge base for organizing and sharing what you learn."
description: >-
  Knolagebase is a free, public web app for building a personal knowledge
  base — capture notes, link ideas together, and search everything from one
  place. No account required to browse.
category: Web App
tags: [free, tool, knowledge, notes]
status: live              # live | beta | archived
url: https://jemmonsss.github.io/Js-Knolagebase/
repo: https://github.com/jemmonsss/Js-Knolagebase
featured: true
date: 2026-07-16
# image field intentionally omitted: the card shows a live <iframe> preview
# of the actual site (https://jemmonsss.github.io/Js-Knolagebase/).
accent: "#a855f7"
layout: default
---

<article class="project-page">
  <h1>{{ page.title }}</h1>
  <p class="tagline">{{ page.tagline }}</p>

  {{ content }}

  Knolagebase helps you turn scattered notes into a connected, searchable
  knowledge base. Add entries, link related topics, and revisit what you've
  learned — all from a clean, fast web interface.

  <div class="links">
    {% if page.url and page.url != empty %}
      <a class="btn btn-primary" href="{{ page.url }}" target="_blank" rel="noopener">Live site</a>
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
