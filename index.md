---
layout: default
title:
nav: home
description: BioEfficiency Lab @ TU Delft.
---

<article class="post featured">
  <header class="major">
    <span class="date">The group</span>
    <h2>Understanding and designing<br />biological efficiency</h2>
    <p>
      We study biological efficiency across scales by combining mitochondrial
      bioenergetics, quantitative physiology and bioengineering. Our work
      connects fundamental insight into metabolism and energy conservation with
      applied research on cell factories and bioprocesses.
    </p>
  </header>

  <div class="team-photo-hover image main" aria-label="BioEfficiency Lab team photos">
    <img src="{{ '/images/team_photo.jpg' | relative_url }}"
         alt="BioEfficiency Lab team" class="photo-main" />
    <img src="{{ '/images/team_photo2.jpg' | relative_url }}"
         alt="BioEfficiency Lab team, alternate photo" class="photo-hover" />
  </div>
</article>

<section class="lab-section">
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
          <p>{{ pillar.description }}</p>
        </div>
        <figure class="pillar-image">
          <img src="{{ '/images/' | append: pillar.image | relative_url }}"
               alt="{{ pillar.image_alt }}" />
        </figure>
      </article>
    {% endfor %}
  </div>
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
      <p>Meet the researchers and students working across organisms, technologies and scales.</p>
    </div>
    <div class="col-4 col-12-small">
      <h3><a href="{{ '/output/' | relative_url }}">Output</a></h3>
      <p>Explore research connecting quantitative biology, bioenergetics and biotechnology.</p>
    </div>
    <div class="col-4 col-12-small">
      <h3><a href="{{ '/positions/' | relative_url }}">Join us</a></h3>
      <p>Learn about student projects, funded vacancies and research collaborations.</p>
    </div>
  </div>
</section>
