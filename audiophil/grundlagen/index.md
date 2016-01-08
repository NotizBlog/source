---
layout:  default
title:   "Grundlagen"
category: AudiophileGrundlagen
tags:    "Audiophile,Grundlagen,"
excerpt: "Rund um die PC HiFi Welt"
---
# Grundlagen.
  <ul class="post-list">
    {% for post in site.posts %}
    {% if post.categories contains 'AudiophileGrundlagen' %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
      </li>
    {% endif %}
    {% endfor %}
  </ul>