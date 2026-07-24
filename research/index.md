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

<section class="post lab-section funding-section">
  <header class="major section-heading">
    <span class="date">Support</span>
    <h2>Funding</h2>
    <p>
      Our research has been supported by the following organizations.
    </p>
  </header>

  <div class="funding-grid">
    <figure class="funding-partner">
      <div class="funding-logo">
        <img src="{{ '/images/funding/fapesp.png' | relative_url }}"
             alt="FAPESP logo" />
      </div>
      <figcaption>FAPESP</figcaption>
    </figure>

    <figure class="funding-partner">
      <div class="funding-logo">
        <img src="{{ '/images/funding/schmidt-sciences.png' | relative_url }}"
             alt="Schmidt Sciences logo" />
      </div>
      <figcaption>Schmidt Sciences</figcaption>
    </figure>

    <figure class="funding-partner">
      <div class="funding-logo">
        <img src="{{ '/images/funding/tu-delft.png' | relative_url }}"
             alt="TU Delft logo" />
      </div>
      <figcaption>TU Delft</figcaption>
    </figure>

    <figure class="funding-partner">
      <div class="funding-logo">
        <img src="{{ '/images/funding/nwo.png' | relative_url }}"
             alt="Dutch Research Council (NWO) logo" />
      </div>
      <figcaption>Dutch Research Council (NWO)</figcaption>
    </figure>

    <figure class="funding-partner">
      <div class="funding-logo">
        <img src="{{ '/images/funding/nationaal-groeifonds.png' | relative_url }}"
             alt="National Growth Fund logo" />
      </div>
      <figcaption>National Growth Fund</figcaption>
    </figure>
  </div>
</section>
