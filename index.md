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
      We study biological efficiency across scales by combining quantitative
      physiology, mitochondrial bioenergetics and bioengineering. Our work
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

  <ul class="actions special">
    <li><a href="{{ '/research/' | relative_url }}" class="button large">Explore our research</a></li>
  </ul>
</article>

<section class="lab-section">
  <header class="major section-heading">
    <span class="date">Research</span>
    <h2>Three complementary pillars</h2>
    <p>
      Our projects connect first-principles understanding with quantitative
      measurement and purposeful biological design.
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
        <p>{{ item.text }}</p>
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

<section class="lab-callout">
  <h2>Interested in working with us?</h2>
  <p>We welcome students, researchers and collaborators who share our interest in biological efficiency.</p>
  <a href="{{ '/positions/' | relative_url }}" class="button large">Explore opportunities</a>
</section>
