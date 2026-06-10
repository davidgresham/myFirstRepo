# Statistical Computing in R

A collection of R scripts and notebooks exploring statistical concepts.

## Contents

### `sampling_distribution.Rmd` — The Sampling Distribution of the Mean

An R Notebook demonstrating the **Central Limit Theorem (CLT)** through simulation.

The notebook builds intuition by:

1. **Creating a non-normal population** — 100,000 draws from a right-skewed exponential distribution, so the starting shape is clearly not bell-curved.
2. **Simulating repeated sampling** — draws 1,000 independent random samples from that population at three different sample sizes (n = 5, 30, 100) and computes the mean of each sample.
3. **Visualising the sampling distributions** — plots the distribution of those 1,000 sample means per sample size, overlaid with the theoretical normal curve predicted by the CLT (mean = μ, SD = σ/√n).
4. **Showing the standard error decay** — table and plot of how SE = σ/√n shrinks as n grows, illustrating why quadrupling sample size is needed to halve uncertainty.

The key result: even though the underlying population is strongly skewed, the distribution of sample means converges to a normal distribution as n increases — and by n = 100 it tracks the theoretical curve closely.

Rendered output: `sampling_distribution.nb.html` (open in any browser).

### `analysis.R`

Exploratory R script with arithmetic operations, written while learning the basics of R and GitHub.

## Requirements

- R ≥ 4.0
- Packages: `ggplot2`, `dplyr`, `tidyr`, `purrr`, `rmarkdown`, `knitr`

To render the notebook:

```r
rmarkdown::render("sampling_distribution.Rmd")
```
