---
layout: default
title: Software Engineering
permalink: /experience/sde/
---

<div class="experience-page">
  <div class="header">
    <h1 class="display-5 fw-bold">Software Engineering</h1>
  </div>
  <p>A summary of my professional experience in Software Engineering. [Detailed information on my resume]</p>
  <div class="list-group list-group-flush pt-4">
    {% for job in site.data.experience_software_engineering %}
      <div class="list-group-item d-flex p-3 p-md-4">
        {% if job.logo %}
          <div class="company-logo-container me-3">
            <img src="{{ job.logo | relative_url }}" alt="{{ job.company }} logo" class="company-logo">
          </div>
        {% endif %}
        <div class="w-100">
          <div class="d-flex justify-content-between align-items-baseline">
            <h4 class="mb-1 fw-bold">{{ job.company }}</h4>
            <span class="text-muted">{{ job.location }}</span>
          </div>
          {% for role in job.roles %}
            <div class="d-flex justify-content-between mt-2">
              <h5 class="mb-1">{{ role.title }}</h5>
              <span class="text-muted">{{ role.dates }}</span>
            </div>
            <ul class="list-unstyled mt-2">
              {% for bullet in role.bullets %}
                <li>{{ bullet }}</li>
              {% endfor %}
            </ul>
          {% endfor %}
        </div>
      </div>
    {% endfor %}
  </div>
</div>