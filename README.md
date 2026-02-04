# clt-zoo
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

An interactive simulation that visualizes the **Law of Large Numbers (LLN)** and the **Central Limit Theorem (CLT)** across many probability distributions.  
The notebook renders three coordinated panels: (1) running mean, (2) sampling distribution of the sample mean, and (3) standardized mean.

---

## What it shows

- **LLN (single path):**  
  The running mean
  $$\bar X_n=\frac{1}{n}\sum_{i=1}^n X_i$$
  stabilizes around the population mean $\mu$ as $n$ increases.

- **CLT (sampling distribution):**  
  For fixed $N$, repeated sample means satisfy
  $$\bar X_N \approx \mathcal N\!\left(\mu,\frac{\sigma^2}{N}\right)$$
  whenever the variance is finite.

- **Standardized mean:**  
  $$Z_N=\frac{\sqrt{N}(\bar X_N-\mu)}{\sigma} \Rightarrow \mathcal N(0,1)$$
  illustrating the classical CLT in its normalized form.

---

## Key Features

- **Distribution zoo:**  
  Normal, Uniform, Exponential, Gamma, Beta, Lognormal, Laplace, Student-t, Pareto, Bernoulli, Binomial, Poisson, Geometric, Negative Binomial.

- **Fully interactive:**  
  Change distribution, parameters, sample size ($N$), repetitions ($M$), and seed via sliders.

- **Three-panel view:**  
  1. Running mean (LLN)  
  2. Sampling distribution of $\bar X_N$ + CLT Normal overlay  
  3. Standardized mean + $\mathcal N(0,1)$ overlay

- **Theory-aware:**  
  Normal overlays and standardization are automatically disabled when mean or variance is infinite.

---

## Requirements

- Python ≥ 3.9  
- `numpy`, `matplotlib`, `ipywidgets`

```bash
pip install numpy matplotlib ipywidgets
