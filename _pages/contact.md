---
layout: home
permalink: /contact/
title: "Contact"
---

{% include base_path %}

<section class="hero-section">
  <div class="hero-copy">
    <div class="section-label"><span>Contact</span></div>
    <h1>{{ site.author.name }}</h1>
    <p class="intro-text">
      The best way to reach me is by email. I'm happy to hear about collaborations, questions on my
      work, or opportunities in theoretical condensed matter physics.
    </p>
    <ul class="contact-list">
      <li>
        <i class="fas fa-fw fa-envelope" aria-hidden="true"></i>
        <a href="mailto:{{ site.author.email }}">{{ site.author.email }}</a>
      </li>
      <li>
        <i class="fas fa-fw fa-building-columns" aria-hidden="true"></i>
        {{ site.author.employer }}
      </li>
      <li>
        <i class="fas fa-fw fa-location-dot" aria-hidden="true"></i>
        {{ site.author.location }}
      </li>
    </ul>
  </div>
</section>

<section class="home-section" id="profiles">
  <div class="section-heading">
    <div class="section-label"><span>Elsewhere</span></div>
    <h2>Academic profiles</h2>
    <p>You can also find my work and code at these profiles.</p>
  </div>
  <ul class="contact-list contact-list--profiles">
    {% if site.author.orcid %}
      <li>
        <i class="ai ai-orcid ai-fw" aria-hidden="true"></i>
        <a href="{{ site.author.orcid }}">ORCID</a>
      </li>
    {% endif %}
    {% if site.author.github %}
      <li>
        <i class="fab fa-fw fa-github" aria-hidden="true"></i>
        <a href="https://github.com/{{ site.author.github }}">GitHub</a>
      </li>
    {% endif %}
  </ul>
</section>
