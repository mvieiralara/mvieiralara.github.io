---
layout: default
title: Research
nav: research
description: Research pillars of the BioEfficiency Lab.
---

<section class="post">
  <header class="major">
    <span class="date">Research</span>
    <h1>Three complementary pillars</h1>
    <p>
      Bioefficiency is the quantitative study of how living cells acquire,
      convert, allocate and utilize resources across biological scales.
    </p>
    <p>
      We study biological efficiency by combining quantitative measurement,
      mechanistic understanding and purposeful engineering.
    </p>
  </header>

  <div class="posts pillars">
    {% for pillar in site.data.research %}
      <article>
        <header>
          <span class="date">{{ pillar.number }}</span>
          <h2>{{ pillar.title }}</h2>
        </header>
        <div class="pillar-icon icon solid {{ pillar.icon }}"></div>
        <p>{{ pillar.description }}</p>
        <ul class="alt compact-list">
          {% for topic in pillar.topics %}
            <li>{{ topic }}</li>
          {% endfor %}
        </ul>
      </article>
    {% endfor %}
  </div>
</section>
