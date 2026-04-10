---
layout: page
title: Meister Lab Project Brief
permalink: /meister-lab/
description: Task-switching during mouse hunting (Caltech, Summer 2024)
nav: true
nav_order: 8
_styles: >
  .brief-hero {
    border-radius: 1rem;
    padding: 1.2rem 1.25rem;
    margin-bottom: 1.5rem;
    background: linear-gradient(135deg, rgba(92, 118, 255, 0.14), rgba(64, 185, 255, 0.1));
    border: 1px solid rgba(127, 127, 127, 0.24);
  }
  .brief-kicker {
    text-transform: uppercase;
    letter-spacing: 0.08em;
    font-size: 0.78rem;
    margin-bottom: 0.45rem;
    opacity: 0.8;
  }
  .brief-tag-row {
    display: flex;
    flex-wrap: wrap;
    gap: 0.45rem;
    margin-top: 0.65rem;
  }
  .brief-tag {
    font-size: 0.8rem;
    border-radius: 999px;
    padding: 0.2rem 0.62rem;
    border: 1px solid rgba(127, 127, 127, 0.3);
    background: rgba(127, 127, 127, 0.08);
  }
  .brief-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 0.75rem;
    margin-bottom: 1.6rem;
  }
  .brief-card {
    border: 1px solid rgba(127, 127, 127, 0.24);
    border-radius: 0.8rem;
    padding: 0.85rem 0.95rem;
    background: rgba(127, 127, 127, 0.05);
  }
  .brief-card h3 {
    margin: 0 0 0.35rem;
    font-size: 1.02rem;
  }
  .brief-card p {
    margin: 0;
    font-size: 0.92rem;
  }
  .flow-step {
    padding: 0.9rem 0;
  }
  .flow-step + .flow-step {
    border-top: 1px dashed rgba(127, 127, 127, 0.3);
  }
  .flow-step h3 {
    margin-bottom: 0.6rem;
  }
  .brief-note {
    margin-top: 1.2rem;
    border-left: 3px solid rgba(92, 118, 255, 0.7);
    padding-left: 0.8rem;
    opacity: 0.9;
  }
  .report-links {
    margin-top: 1rem;
    display: grid;
    gap: 0.4rem;
  }
  .asset-guide {
    margin-top: 1rem;
    font-size: 0.9rem;
    opacity: 0.85;
  }
---

<section class="brief-hero">
  <p class="brief-kicker">Meister Lab · Caltech · Summer 2024</p>
  <h2>Task-switching during visually guided hunting</h2>
  <p>
    A concise, visual-first brief of my closed-loop mouse-hunting project: build a naturalistic hunting task, capture behavior plus Neuropixel data, and model hidden behavioral states with a GLM-HMM.
  </p>
  <div class="brief-tag-row">
    <span class="brief-tag">Closed-loop behavior</span>
    <span class="brief-tag">Neuropixel 1.0</span>
    <span class="brief-tag">Superior colliculus</span>
    <span class="brief-tag">GLM-HMM</span>
  </div>
</section>

<div class="brief-grid">
  <div class="brief-card">
    <h3>Goal</h3>
    <p>Identify latent internal states that shape hunting behavior.</p>
  </div>
  <div class="brief-card">
    <h3>System</h3>
    <p>Artificial prey evades in real time with probabilistic escape trajectories.</p>
  </div>
  <div class="brief-card">
    <h3>Data</h3>
    <p>Behavioral kinematics + high-density neural recordings collected simultaneously.</p>
  </div>
  <div class="brief-card">
    <h3>Model</h3>
    <p>GLM-HMM used to map transitions between behavioral states.</p>
  </div>
</div>

<div class="flow-step">
  <h3>1) Closed-loop setup</h3>
  {% assign setup_fig = site.static_files | where: "path", "/assets/img/projects/meister-lab/01-closed-loop-setup.png" | first %}
  {% if setup_fig %}
    {% include figure.liquid path="assets/img/projects/meister-lab/01-closed-loop-setup.png" alt="Closed-loop hunting setup figure from report" class="img-fluid rounded z-depth-1" caption="Figure from report: arena, tracking loop, and prey-escape logic." %}
  {% else %}
    <div class="brief-card">
      Upload <code>assets/img/projects/meister-lab/01-closed-loop-setup.png</code> to display this figure.
    </div>
  {% endif %}
</div>

<div class="flow-step">
  <h3>2) Behavioral trajectories</h3>
  {% assign behavior_fig = site.static_files | where: "path", "/assets/img/projects/meister-lab/02-behavioral-trajectories.png" | first %}
  {% if behavior_fig %}
    {% include figure.liquid path="assets/img/projects/meister-lab/02-behavioral-trajectories.png" alt="Behavioral trajectories figure from report" class="img-fluid rounded z-depth-1" caption="Figure from report: representative trajectories and kinematic signatures across trials." %}
  {% else %}
    <div class="brief-card">
      Upload <code>assets/img/projects/meister-lab/02-behavioral-trajectories.png</code> to display this figure.
    </div>
  {% endif %}
</div>

<div class="flow-step">
  <h3>3) State inference and neural correspondence</h3>
  {% assign state_fig = site.static_files | where: "path", "/assets/img/projects/meister-lab/03-glm-hmm-states.png" | first %}
  {% if state_fig %}
    {% include figure.liquid path="assets/img/projects/meister-lab/03-glm-hmm-states.png" alt="GLM-HMM latent states and neural correspondence figure from report" class="img-fluid rounded z-depth-1" caption="Figure from report: inferred latent states and correspondence with superior colliculus activity." %}
  {% else %}
    <div class="brief-card">
      Upload <code>assets/img/projects/meister-lab/03-glm-hmm-states.png</code> to display this figure.
    </div>
  {% endif %}
</div>

<blockquote class="brief-note">
  This page is intentionally short and visual. It summarizes the project arc and key outputs without duplicating the full report.
</blockquote>

<div class="report-links">
  {% assign interim_report = site.static_files | where: "path", "/assets/pdf/meister-lab/interim_report.pdf" | first %}
  {% assign interim_report_2 = site.static_files | where: "path", "/assets/pdf/meister-lab/interim_report_2.pdf" | first %}
  {% assign final_report = site.static_files | where: "path", "/assets/pdf/meister-lab/final_project_paper.pdf" | first %}
  {% if interim_report %}
    <a href="{{ '/assets/pdf/meister-lab/interim_report.pdf' | relative_url }}">Interim report (PDF)</a>
  {% endif %}
  {% if interim_report_2 %}
    <a href="{{ '/assets/pdf/meister-lab/interim_report_2.pdf' | relative_url }}">Interim report 2 (PDF)</a>
  {% endif %}
  {% if final_report %}
    <a href="{{ '/assets/pdf/meister-lab/final_project_paper.pdf' | relative_url }}">Final project paper (PDF)</a>
  {% endif %}
  {% unless interim_report or interim_report_2 or final_report %}
    <div class="brief-card">
      Upload project PDFs to <code>assets/pdf/meister-lab/</code> and links will appear here automatically.
    </div>
  {% endunless %}
</div>

<p class="asset-guide">
  Asset map for this page: place your exported report visuals at
  <code>assets/img/projects/meister-lab/01-closed-loop-setup.png</code>,
  <code>.../02-behavioral-trajectories.png</code>, and
  <code>.../03-glm-hmm-states.png</code>; place the PDFs in
  <code>assets/pdf/meister-lab/</code> using the filenames above.
</p>
