---
layout: default
title: Team
nav: team
description: Members of the BioEfficiency Lab.
---

<section class="post">
  <header class="major">
    <span class="date">People</span>
    <h1>Our team</h1>
    <p>
      A multidisciplinary group working across genes, microorganisms, animal cells,
      and bioreactors.
    </p>
  </header>

  {% assign categories = "Principal Investigator|Postdoctoral Researchers|PhD Candidates|MSc Students|Technicians" | split: "|" %}
  {% for category in categories %}
    <h2 class="team-category">{{ category }}</h2>
    <div class="posts team-grid{% if category == 'Principal Investigator' %} one-item{% endif %}">
      {% for person in site.data.team %}
        {% if person.category == category %}
          <article class="person-card">
            <span class="image fit portrait">
              <img src="{{ '/images/' | append: person.photo | relative_url }}"
                   alt="{{ person.name }}" />
            </span>
            <h2>{{ person.name }}</h2>
            <p class="role">{{ person.role }}</p>
            <p>{{ person.description }}</p>
            {% if person.email %}
              <ul class="actions special">
                <li><a href="mailto:{{ person.email }}" class="button small">Email</a></li>
              </ul>
            {% endif %}
          </article>
        {% endif %}
      {% endfor %}
    </div>
  {% endfor %}
</section>
