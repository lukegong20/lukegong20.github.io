---
layout: research
title: research
headline: Modeling, Learning, and Inference of Neural and Biological Dynamical Systems
permalink: /projects/
description: Mathematical foundations and data-driven methods for biological dynamics and neural computation.
nav: true
nav_order: 3
research_sections:
  - id: nonlinear-dynamics
    title: Nonlinear dynamics and control of biological systems
    nav_title: Biological dynamics and control
    question: How does feedback shape stability, oscillations, and collective behavior, and how can these dynamics be regulated?
    description: Mathematical analysis establishes the principles that guide my work on interacting biological systems.
  - id: adaptive-computation
    title: Computational models of adaptive computation in neuron–astrocyte networks
    nav_title: Neuron–astrocyte computation
    question: How do interactions among neurons, synapses, and astrocytes support learning and decision-making across timescales?
    description: Computational modeling and dynamical systems analysis connect neural-glial interactions to context-dependent computation and adaptive behavior in decision-making.
  - id: dynamics-from-data
    title: Learning and inference from neural population data across modes and timescales
    nav_title: Neural modes and timescales
    question: How can neural population recordings reveal distinct dynamical components and coexisting muti-timescale modes?
    description: Statistical learning and system identification uncover dynamical structure across trials and conditions, infer changes between regimes, and estimate latent timescales.
---

<p class="research-intro">My research combines nonlinear dynamics and control theory, mechanistic modeling, and statistical machine learning to understand complex biological systems. I study how feedback shapes collective behavior, how neuron–astrocyte interactions support adaptive computation, and how neural population recordings reveal dynamical structure across modes and timescales. Together, these directions connect mathematical analysis with models that explain biological mechanisms and methods that learn interpretable dynamics from data.</p>

<nav class="research-perspectives" aria-label="Research perspectives">
  {%- for perspective in page.research_sections -%}
  <a href="#{{ perspective.id }}">{{ perspective.nav_title | default: perspective.title | escape }}</a>
  {%- endfor -%}
</nav>

{%- assign research_projects = site.projects | where: "research", true | sort: "importance" -%}
{%- for perspective in page.research_sections -%}
{%- assign perspective_projects = research_projects | where: "perspective", perspective.id -%}
<section class="research-perspective" id="{{ perspective.id }}" aria-labelledby="{{ perspective.id }}-heading">
  <header class="research-perspective-header">
    <h2 id="{{ perspective.id }}-heading">{{ perspective.title | escape }}</h2>
    <p class="research-question">{{ perspective.question | escape }}</p>
    <p class="research-perspective-description">{{ perspective.description | escape }}</p>
  </header>
  <div class="research-grid{% if perspective_projects.size == 1 %} research-grid--single{% endif %}">
    {%- for project in perspective_projects -%}
    <article class="research-card">
      <div class="research-card-body">
        <p class="research-eyebrow">{{ project.label | escape }}</p>
        <h3><a href="{{ project.url | relative_url }}">{{ project.title | escape }}</a></h3>
        <p>{{ project.description | escape }}</p>
        <div class="research-card-footer">
          <a class="research-more" href="{{ project.url | relative_url }}" aria-label="Explore {{ project.title | escape }}">Explore project <span aria-hidden="true">&rarr;</span></a>
        </div>
      </div>
    </article>
    {%- endfor -%}
  </div>
</section>
{%- endfor -%}
