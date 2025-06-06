---
title: "Stock Market Risk Analysis Tool"
nav_order: 1.7
---
# **Stock Market Risk Analysis Tool (How It Works/Limitations)  📈**

![Screenshot](cvar_screenshot.png)

**I built a tool in python that scrapes live options market data for SPY and calculates/creates plots of the risk neutral probabilities and conditional value at risk pay offs for each corresponding strike price and expiration date.**

<a href="https://colab.research.google.com/drive/1FdBUBQo0pNbDS5p4-FoNMrtGmXn6fh0n?usp=sharing" class="btn btn-primary" role="button" target="_blank">🔗 Try it Here! (No Download Neccessary)</a> <br>

## **What is CVaR?**
CVaR is expected shortfall and is a risk assessment measure. CVaR is derived by taking a weighted average of the losses in the tail of the distribution of possible returns, beyond the value at risk (VaR) cutoff point. It answers the question "If a loss exceeds the VaR threshold, what is the average loss in that worst-case tail?”

My tool uses CVaR upside analysis and answers the question, "“If a gain exceeds the VaR threshold (e.g., SPY ends above a selected strike), what is the average gain conditional on being in that upper set of outcomes?”

![Screenshot](cvar_payoff.png)

In the second graph that the code outputs, it shows an average pay off diagram. This means 

