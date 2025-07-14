---
permalink: /projects/
title: "Projects"
layout: single
author_profile: true
---


Here are some of my recent data science and machine learning projects:

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
      <img src="{{ '/assets/images/nlp.jpg' | relative_url }}" alt="Twitter Sentiment Project">
      <div class="project-card-content">
        <h3>Stock Prediction with Twitter Sentiment</h3>
        <p>Built an ML pipeline to predict stock movements based on tweet sentiment. Strategy outperformed a benchmark in backtests.</p>
        <a href="./project-twitter-sentiment">Read more →</a>
      </div>
    </div>

  <div class="project-card">
      <img src="{{ '/assets/images/pca_header.webp' | relative_url }}" alt="PCA Index Arbitrage">
      <div class="project-card-content">
        <h3>Index Arbitrage using PCA</h3>
        <p>Used Principal Component Analysis to detect index mispricings and design a z-score based mean reversion strategy.</p>
        <a href="./project-pca-strategy">Read more →</a>
      </div>
    </div>

  <div class="project-card">
    <img src="{{ '/assets/images/telco_header.png' | relative_url }}" alt="Telco Churn Project">
    <div class="project-card-content">
      <h3>Customer Churn Prediction for Telco</h3>
      <p>Used machine learning to predict telecom churn, with insights on contract types, services, and support features.</p>
      <a href="./project-telco-churn">Read more →</a>
    </div>
  </div>

  <div class="project-card">
      <img src="{{ '/assets/images/simulator_header.png' | relative_url }}" alt="Strategy Simulator">
      <div class="project-card-content">
        <h3>Operational Strategy Simulator</h3>
        <p>Simulated initiative performance and optimizes ROI or ARR under budget and resource constraints. Includes Monte Carlo analysis.</p>
        <a href="./project-strategy-simulator">Read more →</a>
      </div>
    </div>

  <!-- Add more cards here -->
</div>

<hr>

<p style="font-size: 18px; font-weight: bold; margin-bottom: 0.5rem;">Additional GitHub Projects</p>

<div style="font-size: 15px; line-height: 1.6; color: #444;">

<strong><a href="https://github.com/Ilse-hutten/arima-times-series" target="_blank">ARIMA Time Series Forecasting</a></strong><br>
<em>Uses the ARIMA (AutoRegressive Integrated Moving Average) model for time series forecasting.</em><br><br>

<strong><a href="https://github.com/Ilse-hutten/movie-reviews-classifier" target="_blank">Movie Review Sentiment Classifier</a></strong><br>
<em>Classifies movie reviews as positive or negative using NLP and a Naive Bayes model.</em><br><br>

<strong><a href="https://github.com/Ilse-hutten/gradient-descent-manual" target="_blank">Gradient Descent Manual</a></strong><br>
<em>Implements gradient descent from scratch to understand optimization at a mathematical level.</em><br><br>

<strong><a href="https://github.com/Ilse-hutten/neural-network-finetuning" target="_blank">Neural Network Finetuning & Learning Rate Optimization</a></strong><br>
<em>Explores how optimizers, learning rates, and decay strategies affect model training.</em>

</div>
