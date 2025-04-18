---
title: "Home"
nav_order: 1
---

# Welcome to Aaishah's Projects 🚀 🌍 
> Hi! My name is Aaishah, and I am from San Jose, Bay Area. I am currently an undergrad attending Cal Poly SLO majoring in finance + quantitative analysis and minoring in statistics and law. I have a huge passion for finance, and I’m super interested in the intersection between finance and statistics, and how data analysis can be used for financial modeling or even forecasting market events or macroeconomic trends. My work experience includes 1 year in financial reporting, 9 months in tech sales, and 5 months in digital media as well as 1 year of research experience. I’m actively pursuing opportunities in FP&A or financial analyst roles, where I can apply both my analytical background and strategic mindset. Outside of work, I enjoy day trading, concerts (EDM, indie, R&B), skincare, shopping, and boba.
{: .callout-purple }


This is the homepage of my projects.  
Navigate using the sidebar to explore different sections.

<a href="AaishahAslamResume.pdf" class="btn btn-primary" role="button" target="_blank">📄 My Resume</a>
<br>
<a href="https://github.com/aaishahaslam/projects/tree/main?tab=readme-ov-file" class="btn btn-secondary" role="button" target="_blank">🔗 Link to GitHub Home (Code Files)</a>
<br>
*Website coded in HTML/CSS/JavaScript*
<span style="display:block">
Skills: <span class="label label-excel">EXCEL</span>
<span class="label label-r">R</span>
<span class="label label-python">PYTHON</span>
<span class="label label-sql">SQL</span>
<span class="label label-html">HTML</span>
<span class="label label-css">CSS</span>
<span class="label label-js">JAVASCRIPT</span>
</span>
<hr style="margin-top: 1.5rem; border: none; border-top: 1px solid #e1e4e8;">

<details id="projectDetails" open>
<summary id="toggleLabel"><strong>Click to hide</strong></summary>

<p>
- <a href="./project1/">Retail Sales Forecasting Project 🛍️</a> <br>
<span style="margin-left: 2em; display: block;">
This project investigates which time series model best predicts retail sales in Queensland’s clothing industry using data from the Australian Bureau of Statistics. ETS models were derived based on investigating specific trends and seasonality in the data, and the models were evaluated for their forecasting accuracy. In-sample fit and out-of-sample forecasting were assessed using RMSE, followed by a rolling window cross-validation. Autocorrelation plots were also compared to investigate whether temporal dependence remained in the data.
</span>
</p>

<p>
- <a href="./project2/">Boston House Pricing Prediction Machine Learning Analysis 🏠</a> <br>
<span style="margin-left: 2em; display: block;">
This project examines the key factors influencing Boston home prices using machine learning models (KNN algorithm, step-wise regression, random forest). The goal is to understand which factors drive median home values (medv) and to identify the best predictive model. Stepwise and random forest were used for feature selection, while KNN was used to capture nonlinear, data driven patterns to estimate Boston housing prices. 10-fold cross-validation was used to find different values of k and different sets of predictors, helping identify the most accurate KNN configuration for predicting home values.
</span>
</p>

<p>
- <a href="./project4/">Apple Treasury Duration/Convexity Bond Price Modeling 🍎</a> <br>
<span style="margin-left: 2em; display: block;">
This project graphs the price/yield relationship of an Apple treasury bond maturing in 5/6/2044. Moving the slider displays a sensitivity analysis for rising and falling interest rates at different rates, showing the corresponding duration, convexity, and price movement on the graph. This gives a better understanding of how bond prices react to interest rate changes, and how duration and convexity together provide a more accurate estimate of price sensitivity, especially for larger interest rate movements.
</span>
</p>

<p>
- <a href="./project5/">US Flight Arrivals Forecasting ✈️</a> <br>
<span style="margin-left: 2em; display: block;">
This project compares the forecasting performance of ARIMA models to predict quarterly international flight arrivals from the US. After identifying structures in the data, the series was differenced to achieve stationarity, enabling effective use of autocorrelation (ACF) and partial autocorrelation (PACF) plots to guide manual ARIMA selection. An automated ARIMA was also used for comparison and performance was evaluated using RMSE on test forecasts and a rolling cross-validation. Forecasts from both models were plotted and their performance compared.
</span>
</p>

<p>
- <a href="./project3/">Eli Lilly And Co (LLY) Acquisition Analysis Project 💰</a> (in progress ⏳)<br>
<span style="margin-left: 2em; display: block;">
</span>
</p>

</details>

<script>
const details = document.getElementById('projectDetails');
const label = document.getElementById('toggleLabel');

details.addEventListener('toggle', () => {
label.innerHTML = details.open
? '<strong>🔽 Click to hide</strong>'
: '<strong>▶️ Click to show</strong>';
});
</script>

<hr style="margin-top: 1.5rem; border: none; border-top: 1px solid #e1e4e8;">


