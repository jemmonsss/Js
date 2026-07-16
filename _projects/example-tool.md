---
title: "Example Tool"
tagline: "A free web app that does X."
description: >-
  Longer summary used for the project page and SEO/meta extraction.
category: Web App
tags: [free, tool, automation]
status: live              # live | beta | archived
url: https://example.com
repo: https://github.com/yourname/example-tool
featured: true
date: 2026-07-16
image: /images/projects/example-tool.png
accent: "#a855f7"
layout: default
---

<article class="project-page">
  <h1>{{ page.title }}</h1>
  <p class="tagline">{{ page.tagline }}</p>

  {{ content }}

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
