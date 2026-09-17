---
layout: home
permalink: /
title: "Latu Kalita"
redirect_from:
  - /about/
  - /about.html
---

{% include base_path %}

<section class="hero-section">
  <div class="hero-grid">
    <img class="hero-portrait" src="{{ site.author.avatar | prepend: '/images/' | prepend: base_path }}" alt="{{ site.author.name }}">
    <div class="hero-copy">
      <div class="section-label"><span>Welcome</span></div>
      <h1>{{ site.author.name }}</h1>
      <p class="intro-text">
        I'm a Junior Research Fellow at {{ site.author.employer }}, working on theoretical condensed matter
        physics — the interplay of topology, dissipation, and non-equilibrium dynamics. I'm particularly drawn
        to non-Hermitian physics, Floquet engineering, and entanglement structure in topological phases.
      </p>
      <div class="button-row">
        <a href="{{ base_path }}/publications/" class="btn">Publications</a>
        <a href="{{ base_path }}/cv/" class="btn">CV</a>
        <a href="mailto:{{ site.author.email }}" class="btn">Email</a>
      </div>
    </div>
  </div>
</section>

<section class="home-section" id="research">
  <div class="section-heading">
    <div class="section-label"><span>Research</span></div>
    <h2>What I work on</h2>
    <p>
      My work spans Floquet engineering of higher- and hybrid-order topological phases, non-Bloch band theory and
      the non-Hermitian skin effect, and the entanglement structure of driven, disordered, and monitored fermionic
      systems. I'm extending this towards measurement-induced transitions in Majorana circuits, open quantum
      systems, and field-theoretic descriptions of topological criticality.
    </p>
  </div>
</section>

<section class="home-section" id="highlights">
  <div class="section-heading">
    <div class="section-label"><span>Recent Highlights</span></div>
    <h2>Latest news</h2>
  </div>
  <div class="highlight-grid">
    <div class="card">
      <h3>Paper accepted at PRR</h3>
      <p>"Floquet generation of hybrid-order topology and Z<sub>2</sub>-like bipolar localization" has been accepted modulo correction at Physical Review Research.</p>
    </div>
    <div class="card">
      <h3>CSIR-UGC NET, December 2025</h3>
      <p>Qualified with an All India Rank of 174/22,533, earning JRF and Assistant Professor eligibility.</p>
    </div>
    <div class="card">
      <h3>GATE Physics 2025</h3>
      <p>Qualified with All India Rank 325/19,225.</p>
    </div>
    <div class="card">
      <h3>IIT-JAM Physics 2023</h3>
      <p>Qualified with All India Rank 271/12,740.</p>
    </div>
  </div>
</section>

<section class="home-section" id="publications-preview">
  <div class="section-heading">
    <div class="section-label"><span>Publications</span></div>
    <h2><a href="{{ base_path }}/publications/">Recent Papers</a></h2>
    <p>A selection of recent preprints and manuscripts — see the <a href="{{ base_path }}/publications/">publications page</a> for the full list.</p>
  </div>
  <div class="pub-grid">
    {% assign recent_pubs = site.publications | sort: 'date' | reverse %}
    {% for pub in recent_pubs limit:4 %}
      <a class="card" href="{{ base_path }}{{ pub.permalink }}">
        <h3>{{ pub.title }}</h3>
        <p>{{ pub.excerpt | strip_html }}</p>
        <span class="card-meta">{{ pub.venue }}</span>
      </a>
    {% endfor %}
  </div>
</section>
