---
title: "mortselect"
researchkind: software
description: "An R package for mortality forecasting with population selection, age-specific band selection, and ensemble methods, accompanied by an interactive forecast explorer."
summary: "An R package for mortality forecasting through population selection, age-specific band selection, and bivariate ensembles. Its web interface compares saved forecasts by age, population, and year, with interactive charts and CSV/SVG downloads."
hidemeta: true
---

[R package & source code](https://github.com/HG-KaiBai/mortselect) · [Open web interface](https://hg-kaibai.github.io/mortselect/)

## R Package

**mortselect** implements mortality forecasting methods that use data-driven selection and information borrowing across populations and ages. The package brings together three published methodological workflows:

- **Deletion-substitution-addition (DSA):** population selection for mortality forecasting.
- **Age-specific band selection (ASB):** age-band selection for single- and multi-population forecasts.
- **Bivariate model-based ensembles (BMBE):** ensemble forecasts using ACF- and CBD-type base learners.

The package supports data preparation, model fitting, validation, and forecasting, with configurable age ranges, study periods, population exclusions, and forecast horizons.

## Web Interface

The **Mortality Forecast Explorer** provides interactive comparisons of saved forecasts by age, population, and year. It includes method-specific filters, a log scale, shareable views, and CSV/SVG downloads. The interface runs entirely in the browser and displays precomputed forecasts; new models and forecasts can be generated with the R package.

## Authors

Yixing Zhao (author and maintainer), Liqun Diao, Yechao Meng, and Chengguo Weng.
