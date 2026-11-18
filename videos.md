---
layout: page
title: Videos
permalink: /videos/
lede: Short walkthroughs of the same labs and concepts covered in the projects and posts.
---

<div class="notice" role="status">
  <p class="kicker">Coming soon</p>
  <h2>No videos yet</h2>
  <p>Walkthroughs are planned. This page will collect them once they’re published.</p>
  {% assign channel = site.youtube_url | strip %}
  {% if channel.size > 0 %}
  <p>
    <a class="button button-primary" href="{{ channel }}" target="_blank" rel="noopener noreferrer">
      Visit the channel
      <span class="visually-hidden">(opens in a new tab)</span>
    </a>
  </p>
  {% endif %}
</div>
