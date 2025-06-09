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

My tool uses **CVaR upside analysis** and answers the question, **"If a gain exceeds the VaR threshold (e.g., SPY ends above a selected strike), what is the average gain conditional on being in that upper set of outcomes?”**

![Screenshot](cvar_visual.png)

For this example, say we choose strike price 555 and expiration date 10/31/2025 for today (code ran in spring 2025)

In the first graph that the code outputs, it shows the **CVaR region** in green and shows the **probabality** that SPY will end below strike price (k) 555 at the expiration of October 31, 2025 which is 19.90%.  The blue line traces out the **implied cumulative distribution** under the risk-neutral measure. It's jagged at some points due to sparse data or noise. The green region is the region for calculating CVaR.

![Screenshot](cvar_payoff.png)

In the second graph that the code outputs, it shows the **average payoff** conditional on that 19.90% probability. There's a 80.1% that SPY finishes above strike price 555, and the average expected pay off is approximately 44.84 (this is before subtracting the premium paid for the option contract)

## What is VaR?

VaR or value at risk is the given threshold for CVaR. It answers "what is the worse-case loss I can expect with __% confidence over a given time?"

In this tool, **VaR combined with CVaR**, answers the question, **"What is the average gain I can expect if SPY lands in the top 5% of possible outcomes (upper tail)?"**

In the previous two graphs, we **manually set the strike = VaR.** Now in the third graph, we **derive the strike corresponding to a 5% tail (α = 0.95) based on the risk-neutral distribution implied by market option prices.** This gives us the strike that the market believes has only a 5% chance of being exceeded, making it the **natural VaR threshold.** The CVaR is then computed by taking the **average payoff across all strike prices beyond that VaR point to find the expected average payoff if SPY reached the top 5% tail outcomes.**



## Where do the probabilities come from?

The probabilities come from differentiating option prices with respect to strike which allows us to extract the implied risk neutral distrubtion of SPY at expiration. Options reflect forward looking market expectations of what the market thinks SPY will be worth at expiration under a risk neutral measure. This is the risk neutral distribution **embedded** in option prices. 

The risk neutral distribution is embedded in options due to no-arb pricing theory that assumes all assets grow at risk free rate when discounting under risk neutral measure. From there, you can back out cumulative probabilites from observed option prices. In practice, you'd use real world measure; however risk neutral measure is a good **proxy** for shorter time frames. The difference between risk neutral and real world diminishes as time approaches 0 (shorter time frames). Under real world probabilities, CVaR is lower than under risk neutral probabilities. 

The methodology comes from Giovanni Barone Adesi papers which uses European put option to extract the implied risk neutral distribution of asset prices at expiration. I take this methodology and use American call options to extract these distributions. Most models require assumptions about the distribution of returns, but here we directly extract this distribution based on forward looking expectations of the market embedded in option pricing.

Since the probablity extracted from option prices is the discounted version of that probability, we have to undo the discounting to get the **raw probability** at expiration. This means that we will get the risk neutral probability at expiration instead of in today's terms. The code undos the discounting as well giving the raw probability at maturity. 

## Hows it different from delta?

Delta gives a pointwise slope with respect to price, while f(K) gives the full risk-neutral probability density over strikes, which is essential to integrate and compute expected losses or gains. This allows you to look across multiple outcomes, weighted by their likelihood which allows you to calculate CVaR.

![Screenshot](cvar_equation.png)

## More on the theory here:

https://www.proquest.com/docview/2124659891?pq-origsite=gscholar&fromopenview=true&sourcetype=Scholarly%20Journals
