---
layout: default
title: News
nav: news
description: News from the BioEfficiency Lab.
---

<section class="post">
  <header class="major">
    <span class="date">From the lab</span>
    <p>
      Updates on new colleagues, research projects and activities from the
      BioEfficiency Lab.
    </p>
  </header>

  <div class="news-grid">
    {% for item in site.data.news %}
      <article>
        <span class="date">{{ item.date }}</span>
        <h2>{{ item.title }}</h2>
        {% if item.text %}
          <p>{{ item.text }}</p>
        {% endif %}
      </article>
    {% endfor %}
  </div>
</section>
