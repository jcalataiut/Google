# README: Custom Dirichlet Process Mixture Model

## Introduction
This repository contains RMarkdown documents that demonstrates how to create and fit a custom mixture model using the Dirichlet Process. 
The document provides step-by-step explanations, R code implementations, and visualizations of the posterior distributions.

## Tasks Overview

### Easy Task: Fitting a Dirichlet Process Normal Mixture Model
- Install and load the `dirichletprocess` package.
- Fit a normal mixture model to the `faithful` dataset.
- Visualize the resulting distribution.

### Medium Task: Fitting a Multivariate Normal Model
- Fit a multivariate normal mixture model using a Dirichlet Process.
- Apply the model to datasets such as `iris` or `palmerpenguins`.
- Generate and plot the posterior distribution.

## Implementation Details

### Custom Mixing Distribution
- Define a custom Normal-Inverse Gamma mixture distribution.
- Implement functions for:
  - Sampling from the custom mixture model.
  - Computing the log-likelihood function.

### Data Generation and Model Fitting
- Simulate synthetic data from a two-component normal mixture.
- Fit a Dirichlet Process Mixture Model (DPMM) to the data.
- Sample from the posterior and compute 5%/95% quantiles.

### Visualizing Results
- Use `ggplot2` to plot:
  - The posterior distribution of the fitted model.
  - The effect of different priors on the alpha parameter.
  - The convergence of the alpha parameter chains over iterations.

## Equations
The mixture model follows a Normal-Inverse Gamma prior:

$$
\mu | \sigma^2 \sim N(\mu_0, \sigma^2 / \lambda) \\
\sigma^2 \sim IG(\alpha, \beta)
$$

The likelihood function is:

$$
P(y | \mu, \sigma^2) = \prod_{i=1}^{n} \frac{1}{\sqrt{2\pi\sigma^2}} \exp \left(-\frac{(y_i - \mu)^2}{2\sigma^2} \right)
$$

## Requirements
- R version 4.0 or later
- Packages: `dirichletprocess`, `ggplot2`, `knitr`, `dplyr`

## Running the Code
- Open the RMarkdown document in RStudio.
- Run all chunks sequentially to reproduce the results.

## Conclusion
This repository provides a detailed guide to implementing Dirichlet Process Mixture Models in R, demonstrating their flexibility in modeling complex data distributions. The approach allows for Bayesian nonparametric clustering and can be extended to other applications.

