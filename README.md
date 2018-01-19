---
title: "Simple Linear Model"
output: html_notebook
---

## The Basic Model

A measurement instrument produces a response (millivolts) that relates to the true concentration of a contaminant in water. Rather than calibrate the instrument to learn about the relationship, we're going to define the relationship & simulate some calibration data that behave according to that relationship.

Here's the statistical model:

* When the contaminant is absent, the expected response is **b**
* For every ppb increase in concentration, the response increases by **m**
* Instrument response has error (noise) that does not depend on concentration. This noise has mean zero and standard deviation **sigma**.

Another way to describe the model:

* x = concentration, y = response
* y = b + m * x + error
* error ~ dnorm(0, sigma)

## Define Model Parameters

Below, define the model parameters, but using better names than "m" and "b".

```{r}
intercept <- -10
slope <- 1
sigma <- 10
```


