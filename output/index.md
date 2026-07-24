---
layout: default
title: Output
nav: output
description: Research output from the BioEfficiency Lab.
---

<section class="post">
  <header class="major">
    <span class="date">Research outputs</span>
    <h1>Output</h1>
    <p>
      Research connecting fundamental metabolism, quantitative biology and
      sustainable biotechnology.
    </p>
  </header>

  <header class="major section-heading">
    <h2>Publications</h2>
  </header>

  <div class="publication-list">
    {% for publication in site.data.publications %}
      <a class="output-card" href="{{ publication.doi }}"
         target="_blank" rel="noopener"
         aria-label="View {{ publication.title }} on the journal website">
        <article>
          <span class="year">{{ publication.year }} · {{ publication.journal }}</span>
          <h3>{{ publication.title }}</h3>
          <p>{{ publication.authors }}</p>
        </article>
      </a>
    {% endfor %}
  </div>

  <ul class="actions special">
    <li>
      <a href="{{ site.social.scholar }}" target="_blank" rel="noopener"
         class="button large">View Google Scholar</a>
    </li>
  </ul>
</section>

<section class="post lab-section">
  <header class="major section-heading">
    <h2>Patents</h2>
  </header>

  <div class="publication-list">
    {% for patent in site.data.patents %}
      <a class="output-card" href="{{ patent.url }}"
         target="_blank" rel="noopener"
         aria-label="View patent {{ patent.number }}">
        <article>
          <span class="year">{{ patent.year }} · {{ patent.number }}</span>
          <h3>{{ patent.title }}</h3>
          <p>{{ patent.inventors }}</p>
        </article>
      </a>
    {% endfor %}
  </div>
</section>
