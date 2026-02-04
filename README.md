# clt-zoo
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

An interactive, simulation-based visualization of the **Law of Large Numbers (LLN)** and the **Central Limit Theorem (CLT)** across a wide class of probability distributions.  
The repository renders three coordinated panels—(1) running mean (LLN), (2) sampling distribution of the sample mean (CLT), and (3) standardized mean—under user-controlled parameters.

---

## What it shows

- **LLN (single path):**  
  For a single realization,
  $$
  \bar X_n = \frac{1}{n}\sum_{i=1}^n X_i,
  $$
  the running mean stabilizes around the population mean $\mu$ as $n$ grows.

- **CLT (sampling distribution):**  
  For fixed $N$, the empirical distribution of $\bar X_N$ over repeated experiments satisfies
  $$
  \bar X_N \approx \mathcal N\!\left(\mu,\frac{\sigma^2}{N}\right),
  $$
  whenever $\sigma^2<\infty$.

- **Standardized mean:**  
  The standardized statistic
  $$
  Z_N = \frac{\sqrt{N}(\bar X_N-\mu)}{\sigma}
  $$
  converges in distribution to $\mathcal N(0,1)$ under the classical CLT assumptions.

The notebook makes these asymptotic results **visible**, **interactive**, and **distribution-agnostic**.

---

## Key Features

- **Broad distribution zoo:**  
  Normal, Uniform, Exponential, Gamma, Beta, Lognormal, Laplace, Student-t, Pareto, Bernoulli, Binomial, Poisson, Geometric, Negative Binomial.

- **True interactivity:**  
  Distribution choice, parameters, sample size ($N$), repetitions ($M$), and random seed are adjustable via sliders.

- **Three-panel academic layout:**  
  1. Running mean (LLN)  
  2. Sampling distribution of $\bar X_N$ with CLT Normal overlay  
  3. Standardized mean with $\mathcal N(0,1)$ overlay (shown only when valid)

- **Finite-variance logic enforced:**  
  Normal overlays and standardization are automatically disabled when $\mu$ or $\sigma^2$ is infinite (e.g. heavy-tailed cases).

- **Publication-style plots:**  
  Serif fonts, arrow axes, restrained color palette (deep blue), no decorative clutter.

---

## Methodological Notes

- **Model.**  
  $$
  X_i \sim F,\quad i=1,\dots,n,\quad \text{i.i.d.}
  $$
  with mean $\mu$ and variance $\sigma^2$ (if finite).

- **LLN panel.**  
  Illustrates convergence in probability:
  $$
  \bar X_n \xrightarrow{p} \mu.
  $$

- **CLT panel.**  
  Builds $\{\bar X_N^{(j)}\}_{j=1}^M$ from $M$ independent samples of size $N$ and overlays the theoretical CLT approximation.

- **Standardization panel.**  
  Visualizes the convergence
  $$
  \frac{\sqrt{N}(\bar X_N-\mu)}{\sigma} \Rightarrow \mathcal N(0,1),
  $$
  highlighting when and why this fails for infinite-variance distributions.

---

## Requirements

- Python ≥ 3.9  
- Packages: `numpy`, `matplotlib`, `ipywidgets`

Install:
```bash
pip install numpy matplotlib ipywidgets
