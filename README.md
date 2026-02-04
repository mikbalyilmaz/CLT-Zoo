# clt-zoo
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

An interactive simulation that visualizes the **Law of Large Numbers (LLN)** and the **Central Limit Theorem (CLT)** across a wide range of probability distributions.  
The notebook renders three coordinated panels:
1) running mean (LLN)  
2) sampling distribution of the sample mean  
3) standardized mean (CLT)

---

## What it shows

- **LLN (single path):**  
  The running mean  
  `X̄_n = (1/n) * Σ_{i=1}^n X_i`  
  stabilizes around the population mean `μ` as `n` increases.

- **CLT (sampling distribution):**  
  For fixed `N`, repeated sample means satisfy  
  `X̄_N ≈ Normal( μ, σ² / N )`  
  whenever the population variance is finite.

- **Standardized mean:**  
  `Z_N = sqrt(N) * (X̄_N − μ) / σ  →  Normal(0, 1)`  
  illustrating the classical CLT in normalized form.

---

## Key Features

- **Distribution zoo:**  
  Normal, Uniform, Exponential, Gamma, Beta, Lognormal, Laplace, Student-t, Pareto, Chi-square, F,  
  Bernoulli, Binomial, Poisson, Geometric, Negative Binomial.

- **Fully interactive:**  
  Change the distribution, its parameters, sample size (`N`), number of Monte Carlo replications (`M`), and seed using sliders.

- **Three-panel view:**  
  1. Running mean (LLN)  
  2. Sampling distribution of `X̄_N` + Normal (CLT) overlay  
  3. Standardized mean + `Normal(0,1)` overlay

- **Theory-aware:**  
  Normal overlays and standardization are automatically disabled when the mean or variance is infinite (e.g., heavy-tailed cases).

---

## Requirements

- Python ≥ 3.9  
- `numpy`  
- `matplotlib`  
- `ipywidgets`

```bash
pip install numpy matplotlib ipywidgets
