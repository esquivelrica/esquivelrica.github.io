---
title: "HII Mission Technologies"
permalink: /internships-hii/
layout: single
header:
  overlay_image: /assets/images/hiiship.jpg 
  overlay_filter: 0.25
  caption: "USS John C. Stennis (CVN-74) Refueling and Complex Overhaul (RCOH) Tour"
---

June 2024 – August 2024

<section class="tech-stack">
  <h2>Tech Stack</h2>
  <div class="tech-logos">
    <img src="{{ '/assets/logos/python.svg' | relative_url }}"          alt="Python" title="Python">
    <img src="{{ '/assets/logos/jupyter.svg' | relative_url }}" alt="Jupyter Notebook" title="Jupyter Notebook">
    <img src="{{ '/assets/logos/pandas.svg' | relative_url }}" alt="Pandas" title="Pandas">
    <img src="{{ '/assets/logos/numpy.svg' | relative_url }}" alt="Pandas" title="NumPy">
    <img src="{{ '/assets/logos/matplotlib.svg' | relative_url }}" alt="Pandas" title="Matplotlib">
    <img src="{{ '/assets/logos/scikitlearn.svg' | relative_url }}" alt="Scikit-learn" title="Scikit-learn">
    <img src="{{ '/assets/logos/gensim.png' | relative_url }}" alt="Pandas" title="Gensim">
    <img src="{{ '/assets/logos/github.svg' | relative_url }}" alt="GitHub" title="GitHub">
  </div>
</section>

---
## Overview
At HII Mission Technologies (June–August 2024), I built predictive analytics and NLP solutions to support fleet sustainment. My work centered on (1) forecasting **maintenance duration** to reduce downtime and (2) surfacing **actionable insights** from unstructured maintenance notes via a Doc2Vec-based recommender. I packaged outputs into an interactive dashboard with a **3D digital twin** concept to visualize sustainment health and asset readiness.

## Key Contributions
- **Maintenance Duration Modeling:** Trained a **Random Forest** model on historical work orders, parts usage, timestamps, and asset metadata; tuned for MAE and practical interpretability.
- **NLP Recommender (Doc2Vec):** Built a pipeline to normalize/clean free-form notes, learn document vectors, and recommend **similar past cases** to assist maintainers.
- **Interactive Dashboard:** Delivered a **Plotly/Dash** app (with a 3D twin view) to monitor asset status, highlight risk, and drill down to job histories.
- **Data Engineering:** Created reproducible feature pipelines (Pandas/NumPy) and evaluation reports; documented assumptions, data quality checks, and model limitations.
- **Stakeholder Demos:** Presented findings and walked through decision flows with sustainment leads to align outputs with day-to-day operations.

## Impact
- Helped **reduce downtime** by prioritizing long-lead jobs and improving schedule visibility.
- Enabled **faster troubleshooting** by recommending relevant historical work orders from free-text notes.
- Provided a **shared view** (dashboard + 3D twin) for maintainers and leaders to assess readiness at a glance.
---

