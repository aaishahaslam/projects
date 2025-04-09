---
title: "US Flight Arrivals Forecasting"
nav_order: 5
---
# **US Flight Arrivals Forecasting ✈️**

## **Question: Which time series model can better predict international flight arrivals from the US?**

This project is an extension the Retail Sales Prediction project except instead of ETS models, we're comparing an **automated ARIMA and a manually selected ARIMA**. ARIMA models are **AutoRegressive Integrated Moving Average** models that forecast values based on its own past values and past errors. The AR (**auto regressive**) part uses past values to predict current value using a regression on lagged values. The integrated (**differencing**) part removes non-stationarity and the parameter tells us how many times differencing is applied. MA (**moving average**) portion uses past forecast errors to model current values.

p= AR, d= differencing, q = MA

The models are written as ARIMA(p,d,q)(P,D,Q), where the lowercase letters are **non-seasonal** while the uppercase letters are **seasonal**.

**The models we are comparing are an automatically generated ARIMA from R software and an ARIMA ordering we manually chose based on observing autocorrelation and partial autocorrelation plots.**

**Dataset Information**

Quarterly international arrivals to Australia from Japan, New Zealand, UK and the US. 1981Q1 - 2012Q3. We are focusing on **US international flights.**

## Differencing and Model Selection

![autoplot](./us_arrivals_project_files/images/unnamed-chunk-2-1.png)
