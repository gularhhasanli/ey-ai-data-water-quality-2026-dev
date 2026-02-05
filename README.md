# EY AI & Data Challenge 2026 — Clean Water Supply Optimization

## Overview
This project develops a machine learning system to predict river water quality across South Africa using a combination of ground-based measurements, satellite imagery, and climate data. The objective is to support proactive, data-driven water management by forecasting key water quality parameters and identifying the environmental and climatic drivers behind water quality degradation.

This project is developed as part of the **2026 EY AI & Data Challenge**.

---

## Problem Statement
Access to clean and safe water is increasingly threatened by climate variability, land-use change, and human activity. Traditional water quality monitoring systems rely on sparse sampling and often detect problems only after water quality has already degraded.

This project addresses this challenge by building a **spatially transferable machine learning model** capable of predicting water quality at unseen locations and dates. By combining satellite observations, climate indicators, and historical river measurements, the system enables early risk identification and targeted intervention by local water managers and policymakers.

---

## Data

### Target Variables
The model predicts the following continuous water quality parameters:
- **Total alkalinity**
- **Electrical conductance (EC)**
- **Dissolved reactive phosphorus (DRP)**

These parameters are measured at river monitoring stations across South Africa between **2011 and 2015**, curated by UNEP and GEMStat as part of the challenge dataset.

---

### Feature Data
Model features are derived from publicly available datasets, including:
- **Satellite-based land surface indicators** (e.g., Landsat-derived vegetation and land-use proxies)
- **Climate and water balance variables** (e.g., precipitation, temperature, runoff, soil moisture from TerraClimate)
- **Spatial and temporal features** derived from geographic location, seasonality, and historical trends

Additional open-access datasets may be incorporated to improve model performance and spatial generalization.

---

## Approach

### Baseline
The project begins by reproducing the benchmark model provided by the challenge organizers to establish a reference performance level.

### Advanced Modeling
The system is progressively enhanced through:
- Spatiotemporal feature engineering
- Spatially aware cross-validation to reduce geographic leakage
- Target-specific regression models
- Ensemble learning and hyperparameter optimization
- Model interpretability methods to identify key drivers of water quality variation

The focus is on improving **generalization to unseen regions**, which is critical given the challenge validation design.

---

## Evaluation
Model performance is evaluated using the **mean R² score across all three target variables** (alkalinity, EC, DRP), following the official EY AI & Data Challenge evaluation protocol.

Validation is performed on geographically distinct locations to assess spatial transferability rather than memorization.

---

## Reproducibility
The project is designed to be fully reproducible:
- All code is version-controlled
- Raw datasets are not committed to the repository
- Feature generation and model training are deterministic and configurable
- Experiments are logged with configuration details and performance metrics

---

## Repository Structure

<pre>
ey-water-quality-2026/
├── data/
│   ├── raw/          # Raw datasets (not committed)
│   └── processed/    # Processed and feature-engineered data
├── notebooks/        # Jupyter notebooks (EDA, modeling, evaluation)
├── src/              # Reusable Python modules
├── reports/          # Figures, analysis notes, business insights
└── submissions/      # Submission-ready CSV prediction files
</pre>

## Submission
Final predictions are generated as a single CSV file that conforms to the official EY AI & Data Challenge submission template. Each submission corresponds to a fully reproducible experiment logged in the project reports.

## Team
This project is developed by a team of two participants, in accordance with challenge rules. Roles, contributions, and responsibilities are documented transparently.
