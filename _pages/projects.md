---
permalink: /projects/
title: "Projects"
layout: single
author_profile: true
---


Here are some of my public data science projects:

---

<style>
.project-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1.5rem;
  margin-top: 2rem;
}

.project-card {
  border: 1px solid #ddd;
  border-radius: 8px;
  overflow: hidden;
  background: #fff;
  transition: box-shadow 0.2s ease-in-out;
}

.project-card:hover {
  box-shadow: 0 2px 12px rgba(0, 0, 0, 0.1);
}

.project-card img {
  width: 100%;
  height: 170px;
  object-fit: cover;
}

.project-card-content {
  padding: 1rem;
}

.project-card h3 {
  margin-top: 0;
  font-size: 18px;
}

.project-card p {
  font-size: 15px;
  color: #444;
}

.project-card a {
  display: inline-block;
  margin-top: 0.5rem;
  font-weight: bold;
  color: #007acc;
}
</style>

<div style="max-width: 1500px; margin: 0 auto;">
  <div class="project-grid">
    <div class="project-card">
      <img src="{{ '/assets/images/nlp.jpg' | relative_url }}" alt="Relative Value Credit Portfolio">
      <div class="project-card-content">
        <h3>Generating Credit Portfolios with similar behaviour but different price</h3>
        <p>Using CDS spread data and obligor features (industry, rating etc.) to identify portfolios, which behave in similar ways but have significantly different prices.</p>
        <a href="to be added">More to come →</a>
      </div>
    </div>

  <div class="project-card">
      <img src="{{ '/assets/images/pca_header.webp' | relative_url }}" alt="PCA Index Arbitrage">
      <div class="project-card-content">
        <h3>Index Arbitrage using PCA</h3>
        <p>Used Principal Component Analysis to detect index mispricings and design a z-score based mean reversion strategy.</p>
        <a href="./project-pca-strategy">More to come →</a>
      </div>
    </div>

  <div class="project-card">
    <img src="{{ '/assets/images/telco_header.png' | relative_url }}" alt="Flexible Backtester">
    <div class="project-card-content">
      <h3>Strategy backtesting implementation</h3>
      <p>Implemented very flexible backtesting tool with considerations for trading costs, market impacts etc..
      Runs regressions and ML algorithms at each step through time to simulate data available at the time.</p>
      <a href="to be added">Read more →</a>
    </div>
  </div> -->

  <div class="project-card">
      <img src="{{ '/assets/images/simulator_header.png' | relative_url }}" alt="Bank Capital Alllocator">
      <div class="project-card-content">
        <h3>Allocation of capital under constraints</h3>
        <p>Optimizing RoTE under constraints like minimal regulatory level, interactions between measures, liquidity, balance sheet and market stress.</p>
        <a href="to be added">More to come →</a>
      </div>
    </div> -->

  <!-- Add more cards here -->
<!-- </div>

<hr>

<p style="font-size: 18px; font-weight: bold; margin-bottom: 0.5rem;">Additional GitHub Projects</p>

<div style="font-size: 15px; line-height: 1.6; color: #444;">

<strong><a href="https://github.com/mkobers/..." target="_blank">Here needs to go the title</a></strong><br>
<em>Description</em><br><br>

</div> -->
