---
layout: default
title: Team
nav: team
description: Members of the BioEfficiency Lab.
---

<section class="post">
  <header class="major">
    <span class="date">People</span>
    <p>
      A multidisciplinary group working across genes, microorganisms, animal cells,
      and bioreactors.
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

              {% if person.languages %}
                <div class="person-languages">
                  <h3>Languages</h3>
                  <p>{{ person.languages | join: " · " }}</p>
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
        {% endfor %}
      </div>
    {% endif %}
  {% endfor %}
</section>
