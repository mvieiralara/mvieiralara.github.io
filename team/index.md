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
            <div class="person-details">
              <header>
                <h2>{{ person.name }}</h2>
                <p class="role">{{ person.role }}</p>
              </header>

              {% if person.education %}
                <div class="person-background">
                  <h3>Academic background</h3>
                  <ul>
                    {% for degree in person.education %}
                      <li>{{ degree }}</li>
                    {% endfor %}
                  </ul>
                </div>
              {% endif %}

              <div class="person-project">
                <h3>Project</h3>
                <p>{{ person.description }}</p>
              </div>

              {% if person.email %}
                <ul class="actions">
                  <li><a href="mailto:{{ person.email }}" class="button small">Email</a></li>
                </ul>
              {% endif %}
            </div>
          </article>
        {% endif %}
      {% endfor %}
    </div>
  {% endfor %}
</section>
