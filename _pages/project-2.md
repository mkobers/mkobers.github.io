---
permalink: projects/project-pca-strategy/
title: "Index Arbitrage Trading Strategy Using PCA"
layout: single
classes: "container medium"

header:
  overlay_image: /assets/images/pca_header.webp
  overlay_filter: 0.3
---

<h2 style="font-size: 22px; margin-top: 0; color: #333;">Index Arbitrage Trading Strategy Using PCA</h2>

<p style="font-size: 15px; line-height: 1.7; color: #444;">
This project implements a <strong>PCA-based index arbitrage trading strategy</strong> that builds a replication portfolio for major indices (like the FTSE100) and executes mean-reversion trades based on z-score thresholds. Built with Streamlit, the app lets users interactively explore portfolio construction and backtest performance under varying conditions.
</p>

<h3 style="font-size: 18px; color: #333;"> Project Workflow</h3>

<ol style="font-size: 15px; line-height: 1.7; color: #444; padding-left: 20px;">
  <li><strong>Data Collection:</strong> Pulled daily stock prices from BigQuery for index components (e.g., FTSE100, SP500).</li>
  <li><strong>PCA Replication:</strong> Applied Principal Component Analysis to identify stocks most representative of the index (on a rolling basis to adapt to changing index structures).</li>
  <li><strong>Spread Monitoring:</strong> Computed the spread between the index and the replication portfolio returns.</li>
  <li><strong>Z-Score Signal Generation:</strong> Measured spread deviation from its mean to identify entry/exit signals.</li>
  <li><strong>Backtesting:</strong> Simulated trading based on these signals over historical data.</li>
</ol>

<h3 style="font-size: 18px; color: #333;"> What is PCA and How It Helps</h3>

<ul style="font-size: 15px; line-height: 1.7; color: #444;">
  <li><strong>PCA (Principal Component Analysis):</strong> Reduces dimensionality by identifying dominant patterns in the data.</li>
  <li><strong>Replication Logic:</strong> Selects a basket of stocks whose weighted returns approximate the index using top components.</li>
  <li><strong>Spread:</strong> The difference between the log returns of the replication portfolio and the actual index.</li>
</ul>

<h3 style="font-size: 18px; color: #333;"> Example: PCA-Based Replication of FTSE Index </h3>

<p style="font-size: 15px; line-height: 1.7; color: #444;">
Below is a visualization of the <strong>FTSE100 index</strong> versus a <strong>replication portfolio</strong> constructed using the top 5 stocks identified by PCA at a selected point in time.
</p>

<img src="https://mkobers.github.io/my-portfolio/assets/images/replication_ftse.png" alt="FTSE Replication" style="width: 100%; border-radius: 8px; margin: 20px 0;" />

<p style="font-size: 15px; line-height: 1.7; color: #444;">
While the replicated portfolio broadly follows the index, some deviations are visible — primarily due to:
</p>

<ul style="font-size: 15px; line-height: 1.7; color: #444;">
  <li><strong>Static PCA Weights:</strong> The replication is based on PCA applied across the entire date range shown in the plot. While valid for visualization, using this in a trading context would lead to <em>data leakage</em>, since it includes future information not available at decision time.</li>
  <li><strong>Limited Stock Subset:</strong> Only the 5 most representative stocks were used, which naturally introduces tracking error compared to the full FTSE100.</li>
</ul>


<h3 style="font-size: 18px; color: #333;"> Mean Reversion Trading Logic</h3>

<ul style="font-size: 15px; line-height: 1.7; color: #444;">
  <li><strong>Buy:</strong> When z-score &lt; -2 (spread is below the mean by 2 std)</li>
  <li><strong>Sell:</strong> When z-score &gt; 2</li>
  <li><strong>Exit:</strong> When |z-score| &lt; 0.5 (reversion detected)</li>
</ul>

<h3 style="font-size: 18px; color: #333;"> Demo: Streamlit App</h3>

<p style="font-size: 15px; line-height: 1.7; color: #444;">
The app allows you to:
</p>

<ul style="font-size: 15px; line-height: 1.7; color: #444;">
  <li>Select an index and date</li>
  <li>Specify number of stocks and PCA window</li>
  <li>Visualize weights, spreads, and z-score signals</li>
  <li>Backtest the strategy under varying assumptions</li>
</ul>

<video autoplay loop muted playsinline style="width: 100%; border-radius: 8px; margin: 20px 0;">
  <source src="https://mkobers.github.io/my-portfolio/assets/videos/pca_streamlit_demo.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>


<h3 style="font-size: 18px; color: #333;"> Results Snapshot</h3>

<ul style="font-size: 15px; line-height: 1.7; color: #444;">
  <li>Generated consistent z-score signals with reasonable performance over backtest periods.</li>
  <li>Replication portfolios track the index closely using only a subset of stocks.</li>
  <li>Excess returns emerge from mean-reverting behavior in the spread.</li>
</ul>

<h3 style="font-size: 18px; color: #333;"> Limitations</h3>

<ul style="font-size: 15px; line-height: 1.7; color: #444;">
  <li><strong>Linear Assumption:</strong> PCA captures linear correlations only and may ignore more complex nonlinear relationships.</li>
  <li><strong>Mean Reversion Assumption:</strong> The strategy assumes the spread between portfolio and index will revert to the mean (in the near term) — this may not always hold in volatile or trending markets.</li>
  <li><strong>Transaction Costs:</strong> Backtests currently do not include trading costs, which can erode profitability especially in high-turnover environments.</li>
</ul>

<h3 style="font-size: 18px; color: #333;"> Future Improvements</h3>

<ul style="font-size: 15px; line-height: 1.7; color: #444;">
  <li><strong>Incorporate Transaction Costs:</strong> Simulate realistic cost models to better reflect net performance.</li>
  <li><strong>LSTM Models for Spread Prediction:</strong> Integrate sequence models (e.g. LSTM, GRU) to predict spread direction rather than relying solely on z-score thresholds.</li>
  <li><strong>Risk Management:</strong> Add stop-loss logic, volatility filters, or Sharpe-optimized portfolio weighting.</li>
</ul>

<h3 style="font-size: 18px; color: #333;"> Technologies Used</h3>

<ul style="font-size: 15px; line-height: 1.7; color: #444;">
  <li>Python, Streamlit, BigQuery</li>
  <li>scikit-learn (PCA), NumPy, pandas</li>
  <li>Plotly for interactive visualization</li>
</ul>

<p style="margin-top: 10px;">
  <a href="https://github.com/mkobers/index-arbitrage" style="font-size: 16px; color: white; background-color: #007acc; padding: 8px 14px; border-radius: 5px; text-decoration: none;">
    🔗 View on GitHub
  </a>
</p>

<p style="font-size: 15px; line-height: 1.7; margin-top: 30px;">
  <a href="https://mkobers.github.io/my-portfolio/projects/" style="text-decoration: none; color: #007acc;">🔙 Back to Projects</a>
</p>
