---
layout: default
title: Team
nav: team
description: Researchers in bioenergetics, quantitative physiology and mitochondrial engineering at the BioEfficiency Lab.
---

<section class="post">
  <h1 class="visually-hidden">Team</h1>
  <header class="major">
    <span class="date">People</span>
    <p>
      A multidisciplinary group working across genes, mitochondria, yeasts,
      animal cells and bioreactors.
    </p>
  </header>

  {% assign categories = "Principal Investigator|Postdoctoral Researchers|PhD Candidates|Technicians|MSc Students" | split: "|" %}
  {% for category in categories %}
    {% assign category_members = site.data.team | where: "category", category %}
    {% if category_members.size > 0 %}
      <h2 class="team-category">{{ category }}</h2>
      <div class="posts team-grid{% if category == 'Principal Investigator' %} one-item{% endif %}">
        {% for person in category_members %}
          <article class="person-card">
            <span class="image fit portrait">
              {% assign person_photo = person.optimized_photo | default: person.photo %}
              <img src="{{ '/images/' | append: person_photo | relative_url }}"
                   alt="Portrait of {{ person.name }}" loading="lazy"
                   decoding="async" />
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

              {% if person.description %}
                <div class="person-project">
                  <h3>Project</h3>
                  <p>{{ person.description }}</p>
                </div>
              {% endif %}

              {% if person.email or person.about %}
                <div class="person-actions">
                  {% if person.email %}
                    <a href="mailto:{{ person.email }}" class="button small">Email</a>
                  {% endif %}
                  {% if person.about %}
                    <details class="person-about-details">
                      <summary class="button small">About me</summary>
                      <div class="person-about-copy">
                        <p>{{ person.about }}</p>
                      </div>
                    </details>
                  {% endif %}
                </div>
              {% endif %}
            </div>
          </article>
        {% endfor %}
      </div>
    {% endif %}
  {% endfor %}

  <section class="alumni-section">
    <h2 class="team-category">Alumni</h2>

    <div class="alumni-group alumni-graduates">
      <h3>MSc graduates</h3>
      <ul>
        {% for person in site.data.alumni.msc_graduates %}
          <li>
            <span class="alumni-date">{{ person.date }}</span>
            <span>{{ person.name }}{% if person.details %} ({{ person.details }}){% endif %}</span>
          </li>
        {% endfor %}
      </ul>
    </div>

    <div class="alumni-group alumni-guests">
      <h3>Guest researchers</h3>
      <ul>
        {% for person in site.data.alumni.guest_researchers %}
          <li>
            <span class="alumni-date">{{ person.date }}</span>
            <span>{{ person.name }}{% if person.details %} ({{ person.details }}){% endif %}</span>
          </li>
        {% endfor %}
      </ul>
    </div>
  </section>
</section>
