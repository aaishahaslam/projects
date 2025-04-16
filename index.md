---
title: "Home"
nav_order: 1
---

# Welcome to Aaishah's Projects 🚀 🌍 

This is the homepage of my projects.  
Navigate using the sidebar to explore different sections.

<a href="project1/AaishahAslamResume.pdf" class="btn btn-primary" role="button" target="_blank">📄 My Resume</a>
<br>
<a href="https://github.com/aaishahaslam/projects/tree/main?tab=readme-ov-file" class="btn btn-secondary" role="button" target="_blank">🔗 Link to GitHub Repo (Code/Source Files)</a>
<br>

<details id="projectDetails" open>
  <summary id="toggleLabel"><strong>▼ Click to hide</strong></summary>

  <p>- <a href="./project1/">Retail Sales Forecasting Project 📦</a> (COMPLETE ✓)</p>
  <p>
    This project investigates which time series model best predicts retail sales in Queensland’s clothing industry...
  </p>

  <p>- <a href="./project2/">Boston House Pricing Prediction Machine Learning Analysis 🏡</a> (COMPLETE ✓)</p>
  <p>
    This project examines the key factors influencing Boston home prices using machine learning models...
  </p>

  <p>- <a href="./project4/">Apple Treasury Duration/Convexity Bond Price Modeling 🍎</a> (COMPLETE ✓)</p>
  <p>
    This project graphs the price/yield relationship of an Apple treasury bond maturing in 5/6/2044...
  </p>
</details>

<script>
  const details = document.getElementById('projectDetails');
  const label = document.getElementById('toggleLabel');

  details.addEventListener('toggle', () => {
    label.innerHTML = details.open
      ? '<strong>▼ Click to hide</strong>'
      : '<strong>▶ Click to show</strong>';
  });
</script>
