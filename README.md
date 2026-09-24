# Copula Models for Sparse Insurance Losses

**Final project** · MATLAB · Financial Engineering course, Politecnico di Milano

Calibration and backtesting of three Gaussian-copula models for **sparse multivariate insurance claims** on the Danish fire dataset (3 risk classes — Building, Contents, Profits — daily data 1980–1990), where on most days only some classes report a loss.

## What we did

- **Three models** — Zero-Mixed, Comb-Bernoulli (lognormal marginals) and Semi-Parametric Comb-Bernoulli — calibrated by maximum likelihood.
- **Censored copula log-likelihood** with an unconstrained spherical parametrisation of the correlation matrix, vectorised over active-set patterns: full calibration in < 1 s.
- **Parametric bootstrap** (B = 1,000, Bonferroni-corrected) for 95% confidence intervals of all parameters.
- **Daily VaR backtest** 1984–1990, fixed and rolling window, with Kupiec and Christoffersen tests.
- **Extension**: Lomax (power-law) marginals under the same copula fix the tail misfit of the lognormal models; Comb-Bernoulli in arbitrary dimension *d*.

## Repository structure

| Path | Content |
|---|---|
| `Code/RunFINAL_PROJECT.m` | Entry point — runs the whole pipeline |
| `Code/zero_mixed/` | Zero-Mixed model |
| `Code/Comb_and_Semi/` | Comb-Bernoulli and Semi-Parametric models, bootstrap |
| `Code/Backtest/` | Static and rolling-window VaR backtest, coverage tests |
| `Code/Lomax/` | Extension: Lomax marginals |
| `Code/higher_dim/` | Extension: Comb-Bernoulli for arbitrary d |
| `Project6_Copula.pdf` | Project assignment |

## How to run

Open the folder in MATLAB (R2023b or later) and run `Code/RunFINAL_PROJECT.m`. It adds the sub-folders to the path and executes every exercise in order. Each sub-folder of `Code/` has its own README with a file-by-file map.

## Team

Giacomo Costa (group leader), Matteo Montanari, Simone Colombo

Part of the **Financial Engineering** course (Prof. R. Baviera) — M.Sc. in Mathematical Engineering, Quantitative Finance, Politecnico di Milano, A.Y. 2025/26.
