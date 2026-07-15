---
layout: default
title: Publications
nav: publications
description: Publications from the BioEfficiency Lab.
---

<section class="post">
  <header class="major">
    <span class="date">Research outputs</span>
    <h1>Publications</h1>
    <p>
      Research connecting fundamental metabolism, quantitative biology and
      sustainable biotechnology.
    </p>
  </header>

  <div class="publication-list">
    {% assign publications = site.data.publications | sort: "year" | reverse %}
    {% for publication in publications %}
      <article>
        <span class="year">{{ publication.year }} · {{ publication.journal }}</span>
        <h3>{{ publication.title }}</h3>
        <p>{{ publication.authors }}</p>
        {% if publication.doi and publication.doi != "" %}
          <a href="{{ publication.doi }}" class="button small" target="_blank" rel="noopener">DOI</a>
        {% endif %}
      </article>
    {% endfor %}
  </div>

  <ul class="actions special">
    <li>
      <a href="{{ site.social.scholar }}" target="_blank" rel="noopener"
         class="button large">View Google Scholar</a>
    </li>
  </ul>
</section>
