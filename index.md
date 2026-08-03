---
layout: default
title:
nav: home
description: The BioEfficiency Lab at TU Delft studies bioenergetics, quantitative physiology and mitochondrial engineering across biological scales.
---

<article class="post featured">
  <header class="major">
    <span class="date">The group</span>
    <h2>Understanding and designing<br />biological efficiency</h2>
    <p>
      We study biological efficiency across scales by investigating how cells
      conserve and allocate energy. Our work combines bioenergetics,
      quantitative physiology and mitochondrial engineering, connecting
      fundamental mechanisms with cell-factory and bioprocess applications.
    </p>
  </header>

  <div class="team-photo-hover image main" aria-label="BioEfficiency Lab team photos">
    <img src="{{ '/images/optimized/team_photo.jpg' | relative_url }}"
         alt="BioEfficiency Lab team" class="photo-main"
         decoding="async" />
    <img src="{{ '/images/optimized/team_photo2.jpg' | relative_url }}"
         alt="BioEfficiency Lab team, alternate photo" class="photo-hover"
         loading="lazy" decoding="async" />
  </div>
</article>

<section class="lab-section" id="research">
  <header class="major section-heading">
    <span class="date">Research</span>
    <h2>Biological efficiency across scales</h2>
    <p class="research-scale-description">
      From genes, proteins, and metabolism to physiology and bioprocesses
    </p>
    <figure class="research-banner">
      <img src="{{ '/images/banner.png' | relative_url }}"
           alt="From genes and cellular energy systems to quantitative models, engineered cells and bioreactors" />
    </figure>
    <h2>Three complementary pillars</h2>
    <p>
      Our projects connect first-principles understanding with quantitative
      measurement and purposeful biological design.
    </p>
  </header>

  <div class="pillar-rows">
    {% for pillar in site.data.research %}
      <article class="pillar-row">
        <div class="pillar-copy">
          <header class="pillar-heading">
            <h2>{{ pillar.number }}. {{ pillar.title }}</h2>
            <span class="pillar-inline-icon icon solid {{ pillar.icon }}"
                  aria-hidden="true"></span>
          </header>
          <p class="pillar-mode">
            {% case pillar.number %}
              {% when "I" %}Understand
              {% when "II" %}Measure
              {% when "III" %}Engineer
            {% endcase %}
          </p>
          <p>{{ pillar.description }}</p>
        </div>
        <figure class="pillar-image">
          {% assign pillar_image = pillar.optimized_image | default: pillar.image %}
          <img src="{{ '/images/' | append: pillar_image | relative_url }}"
               alt="{{ pillar.image_alt }}" loading="lazy" decoding="async" />
        </figure>
      </article>
    {% endfor %}
  </div>
</section>

<section class="cross-cutting-section">
  <h2>Across the pillars</h2>
  <ul class="cross-cutting-list">
    <li><strong>Alternative feedstocks:</strong> diverse carbon and nutrient sources for sustainable biotechnology.</li>
    <li><strong>Metabolic diversity:</strong> systems-level understanding of distinct metabolic strategies.</li>
    <li><strong>Advanced off-gas analysis:</strong> quantitative cultivation beyond conventional O<sub>2</sub> and CO<sub>2</sub> measurements.</li>
    <li><strong>Bioprocess development:</strong> translation to process-relevant conditions and scale-up.</li>
  </ul>
</section>

{% include funding.html %}

<section class="post lab-section">
  <header class="major section-heading">
    <span class="date">News</span>
    <h2>Latest from the lab</h2>
  </header>
  <div class="news-grid">
    {% for item in site.data.news limit:3 %}
      <article>
        <span class="date">{{ item.date }}</span>
        <h3>{{ item.title }}</h3>
        {% if item.text %}
          <p>{{ item.text }}</p>
        {% endif %}
      </article>
    {% endfor %}
  </div>
</section>

<section class="post lab-section home-links">
  <header class="major section-heading">
    <span class="date">Explore</span>
    <h2>The lab</h2>
  </header>
  <div class="row">
    <div class="col-4 col-12-small">
      <h3><a href="{{ '/team/' | relative_url }}">People</a></h3>
      <p>Meet the researchers and students working across genes, mitochondria, yeast, animal cells and bioreactors.</p>
    </div>
    <div class="col-4 col-12-small">
      <h3><a href="{{ '/output/' | relative_url }}">Output</a></h3>
      <p>Explore research connecting bioenergetics, quantitative physiology and mitochondrial engineering.</p>
    </div>
    <div class="col-4 col-12-small">
      <h3><a href="{{ '/contact/#join-the-lab' | relative_url }}">Join us</a></h3>
      <p>Learn about student projects, funded vacancies and research collaborations.</p>
    </div>
  </div>
</section>
