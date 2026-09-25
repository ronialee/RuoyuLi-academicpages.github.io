---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

<div class="research-accordion">
  <details>
    <summary>Research Experience</summary>
    <div class="research-accordion__content">
      <h2>Early Childhood Education Resources in Chinese Megacities</h2>
      <p><strong>Research Assistant · National Education Sciences Planning Youth Project CHA220301 · September 2024–present</strong></p>
      <p>This project investigates the spatial patterns and governance mechanisms of early childhood education resources in Chinese megacities. The project is supported by RMB 200,000 in funding.</p>
      <ul>
        <li>Retrieved and screened 514 policy documents issued between 2010 and 2024 by 21 Chinese megacities and super-large cities, and coded 5,538 meaning units using NVivo 15.</li>
        <li>Applied a three-dimensional framework of policy instruments, policy domains, and responsible actors to examine resource provision, equitable access, and support for disadvantaged areas and groups.</li>
        <li>Analyzed how existing policy instruments respond to demographic change, population mobility, regional disparities, and multi-actor governance.</li>
        <li>Co-authored two manuscripts arising from the project, serving as first author on one.</li>
      </ul>
      <h2>Children’s Activity Trajectories and Spatial Experiences in Kindergarten</h2>
      <p><em>Master’s Thesis</em> · 2025.12–Present</p>
      <ul>
        <li>Investigating 5–6-year-old children’s spatial activity trajectories and experiences in kindergarten through systematic tracking observation and the Mosaic approach.</li>
        <li>Examining children’s spatial use, preferences, and meaning-making through child-led tours, photography, drawing-based interviews, and route mapping.</li>
        <li>Completed approximately 108 hours of observation, 24 interviews, and 6 child-led tours; coded transcripts of child interviews and child-led tours using grounded theory coding procedures.</li>
      </ul>
    </div>
  </details>

  <details>
    <summary>Publications</summary>
    <div class="research-accordion__content">
      {% if site.publication_category %}
        {% for category in site.publication_category %}
          {% assign title_shown = false %}
          {% for post in site.publications reversed %}
            {% if post.category != category[0] %}
              {% continue %}
            {% endif %}
            {% unless title_shown %}
              <h2>{{ category[1].title }}</h2>
              {% assign title_shown = true %}
            {% endunless %}
            {% include archive-single-publication-plain.html %}
          {% endfor %}
        {% endfor %}
      {% else %}
        {% for post in site.publications reversed %}
          {% include archive-single-publication-plain.html %}
        {% endfor %}
      {% endif %}
    </div>
  </details>

  <details>
    <summary>Conference Presentations</summary>
    <div class="research-accordion__content">
      {% for post in site.talks reversed %}
        {% include archive-single-talk.html %}
      {% endfor %}
    </div>
  </details>
</div>

<style>
  .research-accordion {
    border-top: 1px solid #d7d7d7;
  }

  .research-accordion details {
    border-bottom: 1px solid #d7d7d7;
  }

  .research-accordion summary {
    align-items: center;
    cursor: pointer;
    display: flex;
    font-family: Georgia, Times, serif;
    font-size: 1.35rem;
    font-weight: 700;
    justify-content: space-between;
    list-style: none;
    padding: 1.25rem 0;
  }

  .research-accordion summary::-webkit-details-marker {
    display: none;
  }

  .research-accordion summary::after {
    content: "›";
    display: inline-block;
    font-family: Arial, sans-serif;
    font-size: 1.8rem;
    font-weight: 400;
    line-height: 1;
    margin-left: 1rem;
    transition: transform 160ms ease;
  }

  .research-accordion details[open] summary::after {
    transform: rotate(90deg);
  }

  .research-accordion summary:focus-visible {
    outline: 2px solid #3d5a80;
    outline-offset: 4px;
  }

  .research-accordion__content {
    padding: 0.25rem 0 1.75rem;
  }

  .research-accordion__content h2:first-child {
    margin-top: 0.5rem;
  }

  .research-accordion .publication-summary,
  .research-accordion .publication-summary p {
    font-size: 1rem;
    line-height: 1.65;
  }
</style>
