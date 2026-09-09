<div align="center">

# Seasonal Agriculture Performance Analysis
### An End-to-End Agronomic Analytics & Statistical Modeling Framework

[![Python](https://img.shields.io/badge/Python-3.9%20%7C%203.10%20%7C%203.11-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-2.0%2B-150458?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-1.24%2B-013243?logo=numpy&logoColor=white)](https://numpy.org/)
[![SciPy](https://img.shields.io/badge/SciPy-1.10%2B-8CAAE6?logo=scipy&logoColor=white)](https://scipy.org/)
[![Statsmodels](https://img.shields.io/badge/Statsmodels-0.14%2B-blueviolet)](https://www.statsmodels.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-0.12%2B-4c72b0)](https://seaborn.pydata.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-3.7%2B-11557c)](https://matplotlib.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

<p align="center">
  <b>A comprehensive empirical investigation of 4,000 agricultural farm units across India to evaluate seasonal variance, agro-climatic drivers, resource utilization efficiency, and crop-geographic interaction dynamics.</b>
</p>

</div>

---

<div id="project-overview">
<h2> Executive Summary</h2>
</div>

Agricultural output is fundamentally dictated by seasonal shifts in temperature, precipitation, soil dynamics, resource availability, and operational farm practices. While high-level reporting frequently relies on annualized aggregates, real-world productivity is distributed across distinct seasonal cycles: **Kharif** (Monsoon/Autumn), **Rabi** (Winter/Spring), and **Zaid** (Summer).

This project implements an inferential data analytics and statistical testing pipeline on a multi-dimensional dataset of **4,000 farm profiles spanning 8 states, 10 districts, and 8 crop varieties**. Moving beyond exploratory data analysis, this study formulates hypothesis-driven research questions, assesses parametric and non-parametric statistical assumptions, evaluates interaction effects via Two-Way Factorial ANOVA, profiles severe resource anomalies, and establishes actionable, evidence-based agricultural planning guidelines.

---

<div id="problem-statement">
<h2> Core Problem & Research Objectives</h2>
</div>

### Problem Statement
Raw agricultural data does not natively reveal why productivity fluctuates across seasons, whether resource usage aligns with marginal yield returns, or if geographic and crop-level factors mediate seasonal outcomes[cite: 1]. This initiative was engineered to address the core problem defined by the **VOIS AICTE Major Project Framework**:
> *"Investigate seasonal differences in agricultural performance by identifying meaningful patterns, trends, relationships, and variations within the available data to support evidence-based seasonal agricultural planning."*[cite: 1]

### Analytical Research Questions (AQs)
* **AQ1 (Productivity Gradient):** How do crop yield, volumetric production, water efficiency, and net operational profit vary across Kharif, Rabi, and Zaid seasons[cite: 1]?
* **AQ2 (Environmental Profiling):** Which agro-climatic indicators (temperature, precipitation, relative humidity, solar exposure, soil moisture/pH) distinguish seasonal farming conditions[cite: 1]?
* **AQ3 (Resource Utilization):** How do volumetric water demands, NPK macronutrient loads, and pesticide applications change across seasons, and how does irrigation infrastructure mediate performance[cite: 1]?
* **AQ4 (Environmental vs. Yield Sensitivities):** What linear and non-linear relationships exist between environmental factors and crop yield[cite: 1]?
* **AQ5 (Input Dynamics & Diminishing Returns):** Does higher input consumption generate proportional yield returns, or do inputs exhibit saturation thresholds[cite: 1]?
* **AQ6 (Seasonal Financial Architecture):** How do operating expenditure, gross revenue, and net profit margins vary seasonally, and what drives farm financial distress[cite: 1]?
* **AQ7 (Regional Consistency):** Are seasonal performance dynamics uniform across geographic states, or do regional climates induce significant interaction effects[cite: 1]?
* **AQ8 (Crop-Specific Sensitivity):** Is seasonal productivity consistent across crop varieties, or does seasonality exhibit crop-dependent interactions[cite: 1]?

---

<div id="key-empirical-findings">
<h2> Key Empirical Findings</h2>
</div>

<div align="center">

| Analytical Dimension | Kharif Regime | Rabi Regime | Zaid Regime | Statistical Evidence |
| :--- | :---: | :---: | :---: | :--- |
| **Mean Crop Yield** | **5.64 t/ha** | 5.08 t/ha | 4.67 t/ha | Kruskal-Wallis $H = 68.60$ ($p < 10^{-14}$) |
| **Median Crop Yield** | **1.95 t/ha** | 1.66 t/ha | 1.45 t/ha | Mann-Whitney post-hoc (all $p_{\text{adj}} < 10^{-4}$) |
| **Water Consumption** | 6,094.0 m³ | 5,837.2 m³ | **6,423.1 m³** | Inverse relationship with yield efficiency |
| **Water Efficiency** | **5.91 t/1000m³** | 5.18 t/1000m³ | 4.44 t/1000m³ | Severe resource degradation during summer heat |
| **Mean Farm Profit** | **+179,367 INR** | +88,197 INR | **-26,592 INR** | Significant seasonal financial divergence |
| **Farms in Net Loss** | 42.27% | 51.28% | **64.52%** | High structural distress in Zaid operations |
| **Mean Precipitation** | **885.6 mm** | 486.2 mm | 198.8 mm | Strong agro-climatic shift |
| **Mean Temperature** | 27.8 °C | 22.4 °C | **32.5 °C** | Extreme thermal stress in Zaid |

</div>

### Agronomic & Financial Takeaways
1. **The Seasonal Productivity Hierarchy:** Kharif outperforms Rabi and Zaid across both parametric means and robust non-parametric medians. While high-yielding cash crops (e.g., Sugarcane) elevate overall mean yields, median yields reveal that typical farm productivity remains concentrated below 2.0 t/ha.
2. **The Zaid Resource Paradox:** Farms operating in Zaid consume the highest volume of water ($6,423.08\text{ m}^3$) due to elevated temperatures ($32.54\text{ }^\circ\text{C}$) and minimal rainfall ($198.81\text{ mm}$), yet achieve the lowest water efficiency ($4.44\text{ t/1000m}^3$) and suffer negative average net profits ($-26,592.40\text{ INR}$).
3. **Crop-Season Mediation vs. Regional Stability:**
   * **Regional Consistency ($p = 0.0511$):** A Two-Way Factorial ANOVA ($\text{Yield} \sim \text{Season} + \text{State} + \text{Season}\times\text{State}$) demonstrates that seasonal trajectories do not invert significantly across states[cite: 1].
   * **Crop Interaction ($p = 4.25 \times 10^{-48}$):** Two-Way ANOVA reveals strong crop dependency ($F = 19.45$). High-value cash crops (Sugarcane, Chilli) maintain strong margins year-round, whereas cereals (Rice, Wheat, Maize) suffer severe losses when cultivated in Zaid.
4. **Irrigation Inefficiency:** Flood irrigation accounts for **55.31% of all extreme water consumption anomalies** ($> 14,064.5\text{ m}^3$). In contrast, Drip and Sprinkler systems maintain resilient yields across moisture-deficient periods.

---

<div id="system-architecture--pipeline">
<h2> Pipeline Architecture & Execution Flow</h2>
</div>

The project follows a sequential 10-phase pipeline designed for full determinism and execution reproducibility:

* **Phase 1: Environment Setup, Data Ingestion & Reproducibility Controls**
  * Establishes global deterministic state (`SEED = 42`) across Python, NumPy, and Pandas.
  * Ingests the 4,000-row $\times$ 28-column dataset directly via memory buffer.
  * Audits primary key uniqueness (`Farm_ID`) and verifies physical domain boundary rules.
  * Builds an 8-domain agronomic data dictionary mapping all 28 features.
* **Phase 2: Systematic Preprocessing & Feature Engineering**
  * Target Leakage Prevention: Drops 32 records with unobserved ground truth (`Yield_Tonnes_Ha`).
  * Stratified Imputation: Imputes `Rainfall_mm` using localized `State` $\times$ `Season` medians, and `Soil_Moisture_pct` using seasonal medians.
  * Standardizes categorical features by stripping whitespace and enforcing uniform title casing.
  * Engineers domain-specific features: `Profit_Margin_pct`, `Verified_Land_Productivity`, and `Total_NPK_kg_ha`.
* **Phase 3: Exploratory Data Analysis & Macro Baseline**
  * Computes parametric moments and non-parametric dispersion metrics across core numeric columns.
  * Diagnoses distribution skewness and heavy right tails using density KDE plots and boxplots.
  * Assesses class balance and Shannon entropy across temporal, spatial, and crop categories.
* **Phase 4: Core Seasonal Comparative Analysis (AQ1 – AQ3)**
  * Quantifies mean, standard deviation, median, and IQR for yield, production, water efficiency, and profit.
  * Profiles seasonal agro-climatic shifts across temperature, rainfall, humidity, and soil characteristics.
  * Analyzes volumetric water usage, NPK application rates, and irrigation efficiency by season.
* **Phase 5: Bi-Variate & Multi-Variate Relationship Analysis (AQ4 – AQ6)**
  * Evaluates linear (Pearson $r$) and rank (Spearman $\rho$) correlations against crop yield with exact $p$-values.
  * Models non-linear diminishing returns using second-order polynomial regressions.
  * Deconstructs seasonal financial health: unit operating expenses vs. gross revenue and loss rates.
* **Phase 6: Regional & Crop Interaction Testing (AQ7 – AQ8)**
  * Fits a Two-Way Factorial ANOVA ($\text{Yield} \sim \text{Season} + \text{State} + \text{Season}\times\text{State}$) to test regional consistency[cite: 1].
  * Fits a Two-Way Factorial ANOVA ($\text{Yield} \sim \text{Season} + \text{Crop} + \text{Season}\times\text{Crop}$) to determine crop-level dependency[cite: 1].
* **Phase 7: Formal Inferential Statistics, Assumptions & Effect Sizes**
  * Verifies parametric normality via D'Agostino-Pearson Omnibus tests and normal Q-Q plots.
  * Verifies homoscedasticity using Levene's and Bartlett's variance homogeneity tests.
  * Executes non-parametric Kruskal-Wallis $H$-tests and Bonferroni-adjusted post-hoc pairwise Mann-Whitney $U$ tests.
  * Quantifies effect sizes: Eta-Squared ($\eta^2$), Omega-Squared ($\omega^2$), Cohen's $d$, and Hedges' $g$.
* **Phase 8: Systematic Outlier & Multi-Attribute Anomaly Profiling**
  * Detects univariate outliers via Tukey's $1.5 \times \text{IQR}$ fences and Modified Z-scores ($Z_{\text{MAD}} > 3.5$).
  * Profiles the operational attributes of loss-making farms during peak Kharif production.
  * Analyzes the irrigation methods, soil types, and district clusters associated with severe water waste.
* **Phase 9: Evidence-Based Insights & Data-Driven Recommendations**
  * Synthesizes findings across climate, resources, geography, and crops into validated conclusions[cite: 1].
  * Translates data evidence into 4 concrete agricultural policy and farm management interventions[cite: 1].
* **Phase 10: Conclusion & Jupyter Notebook Documentation**
  * Summarizes primary drivers, statistical limitations, and dataset scope boundaries[cite: 1].
  * Executes automated pipeline assertions verifying record retention, null handling, and feature integrity.

---

<div id="statistical-methodology--assumptions">
<h2> Statistical Methodology & Assumption Testing</h2>
</div>

### 1. Assumption Diagnostics
* **Normality:** Evaluated using the **D'Agostino-Pearson Omnibus test** ($\alpha = 0.05$) alongside normal Q-Q plots. Both `Yield_Tonnes_Ha` ($p < 10^{-50}$) and `Profit_INR` ($p < 10^{-50}$) severely depart from normality due to right-tail skewness.
* **Homoscedasticity:** Evaluated via **Levene's test** (median-centered for skewness tolerance) and **Bartlett's test**. Variance was non-homogeneous across seasons for economic indicators.

### 2. Primary Hypothesis Testing & Non-Parametric Validation
* Standard One-Way ANOVA on raw yield averages resulted in $F = 1.4580$ ($p = 0.2328$), as extreme variance in high-yield crops widened the denominator mean square error.
* The non-parametric **Kruskal-Wallis $H$-test** demonstrated that seasonal yield distributions differ significantly:
  $$\text{Kruskal-Wallis } H = 68.6043, \quad p = 1.267 \times 10^{-15}$$
* Pairwise **Mann-Whitney $U$ tests with Bonferroni correction** confirmed significant differences across all combinations:
  * Kharif vs. Rabi: $U = 1,568,847.5, \quad p_{\text{bonferroni}} = 9.08 \times 10^{-7}$
  * Kharif vs. Zaid: $U = 633,975.5, \quad p_{\text{bonferroni}} = 1.54 \times 10^{-14}$
  * Rabi vs. Zaid: $U = 528,776.0, \quad p_{\text{bonferroni}} = 7.41 \times 10^{-5}$

### 3. Factorial Interaction Models
$$\text{Model 1: } \text{Yield} \sim \text{Season} + \text{State} + \text{Season} \times \text{State} \implies F_{\text{interaction}} = 1.6889, \; p = 0.0511$$
$$\text{Model 2: } \text{Yield} \sim \text{Season} + \text{Crop} + \text{Season} \times \text{Crop} \implies F_{\text{interaction}} = 19.4468, \; p = 4.25 \times 10^{-48}$$

### 4. Effect Size Quantification
* **Model-Level Variance Explained:** Eta-Squared ($\eta^2 = 0.000735$) and Omega-Squared ($\omega^2 = 0.000231$) confirm that Season alone accounts for a modest direct variance share, proving that seasonality must be analyzed in conjunction with Crop variety and Irrigation infrastructure rather than as an isolated driver.
* **Pairwise Standardized Mean Differences:**
  * Kharif vs. Rabi: $\text{Cohen's } d = 0.0412 \quad (\text{Hedges' } g = 0.0412)$
  * Kharif vs. Zaid: $\text{Cohen's } d = 0.0713 \quad (\text{Hedges' } g = 0.0713)$
  * Rabi vs. Zaid: $\text{Cohen's } d = 0.0333 \quad (\text{Hedges' } g = 0.0333)$

---

<div id="actionable-recommendations">
<h2> Actionable Agricultural Planning Protocols</h2>
</div>

<div align="center">

| Operational Domain | Empirical Ground Truth | Strategic Planning Protocol |
| :--- | :--- | :--- |
| **1. Zaid Crop Shifting Protocol** | Cereal crops (Rice: -227,239 INR, Wheat: -193,209 INR, Maize: -191,072 INR) incur heavy losses in Zaid; 64.5% of Zaid farms operate at a net loss. | Establish a moratorium on water-intensive cereal cultivation during Zaid. Transition smallholders to drought-tolerant pulses, groundnut, or high-margin horticulture (Chilli/Sugarcane) paired with micro-irrigation. |
| **2. Volumetric Water Quotas** | Zaid water consumption averages 6,423 m³ with a low efficiency of 4.44 t/1000m³. Flood irrigation accounts for 55.3% of severe water waste outliers. | Implement volumetric groundwater extraction caps in water-stressed districts (e.g., Nalgonda, Rajkot, Indore). Link agricultural power subsidies directly to adoption of pressurized drip/sprinkler systems. |
| **3. Macronutrient Rationalization** | Polynomial regression identifies plateauing returns beyond 300 kg/ha Total NPK, increasing farm operating costs without corresponding yield gains. | Deploy soil-health card-based precision fertilization kits. Cap blanket nitrogen subsidies and incentivize customized NPK blends formulated according to local soil pH profiles. |
| **4. Revenue Index Insurance** | While regional yield patterns are stable across states, 42.3% of Kharif farms operate at a loss due to input cost volatility and pest pressures. | Transition crop insurance triggers from simple yield-loss thresholds to revenue-based index insurance, protecting farmers against input cost inflation and regional price crashes. |

</div>

---

<div id="getting-started">
<h2> Getting Started & Reproduction Guide</h2>
</div>

### Environment Requirements
* Python 3.9, 3.10, or 3.11
* Google Colab or local JupyterLab environment

### Python Dependencies
```text
pandas>=2.0.0
numpy>=1.24.0
scipy>=1.10.0
statsmodels>=0.14.0
matplotlib>=3.7.0
seaborn>=0.12.0







# 🌾 Seasonal Agriculture Performance Analysis

<p align="center">
  <b>Data Analytics • Statistical Modeling • Agricultural Intelligence</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.9%2B-blue?logo=python">
  <img src="https://img.shields.io/badge/Data%20Analytics-Statistical%20Modeling-orange">
  <img src="https://img.shields.io/badge/Dataset-4%2C000%20Farms-green">
  <img src="https://img.shields.io/badge/Seasons-3-success">
  <img src="https://img.shields.io/badge/License-MIT-yellow">
</p>

---

## 📌 Overview

**Seasonal Agriculture Performance Analysis** is a data-driven agricultural analytics project that investigates how farming performance varies across **Kharif, Rabi, and Zaid seasons**.

The study analyzes agricultural, environmental, resource-utilization, and financial variables from **4,000 farms across India** to identify the factors influencing productivity, water efficiency, profitability, and seasonal risk.

The project goes beyond descriptive analysis by combining:

* Exploratory Data Analysis
* Correlation and regression analysis
* Statistical hypothesis testing
* Seasonal comparison
* State and crop interaction analysis
* Outlier and anomaly detection
* Effect-size measurement
* Evidence-based agricultural recommendations

> **Core Question:**
> *How does agricultural performance change across seasons, and what factors explain these differences?*

---

## 🎯 Project Objectives

The project aims to:

1. Compare agricultural performance across **Kharif, Rabi, and Zaid**.
2. Analyze the influence of environmental conditions on crop yield.
3. Examine water, fertilizer, pesticide, and irrigation utilization.
4. Identify linear and non-linear relationships between inputs and productivity.
5. Evaluate whether increasing agricultural inputs produces proportional yield improvements.
6. Compare expenditure, revenue, profit, margin, and loss rates across seasons.
7. Investigate whether seasonal patterns remain consistent across states.
8. Study the interaction between **season and crop selection**.
9. Detect inefficient, high-risk, and anomalous agricultural observations.
10. Convert statistical findings into practical agricultural planning recommendations.

---

## 🌱 Why This Project?

Agricultural productivity is influenced by a combination of **seasonal, environmental, operational, and economic factors**.

Rainfall, temperature, soil conditions, water availability, crop selection, fertilizer usage, irrigation practices, and production costs can vary substantially across seasons.

Understanding these relationships can help identify:

* High-performing seasons
* Resource-intensive farming conditions
* Water-efficiency gaps
* Financially risky farming patterns
* Input-output inefficiencies
* Crop-specific seasonal behavior

This project therefore aims to transform raw agricultural records into **statistically validated insights that support better resource and crop planning**.

---

## 📊 Dataset at a Glance

| Metric                      |              Value |
| --------------------------- | -----------------: |
| Farms                       |          **4,000** |
| Seasons                     |              **3** |
| Geographic Coverage         |          **India** |
| Primary Seasons             | Kharif, Rabi, Zaid |
| Major Analytical Dimensions |            **10+** |
| Statistical Techniques      |             **8+** |

### Seasons Covered

| Season         | General Characteristics                                      |
| -------------- | ------------------------------------------------------------ |
| 🌧️ **Kharif** | Higher rainfall and stronger overall performance             |
| ❄️ **Rabi**    | Moderate environmental conditions                            |
| ☀️ **Zaid**    | Low rainfall, higher temperature, higher irrigation pressure |

---

# 📈 Key Findings

## 🥇 Kharif — Strongest Overall Performance

Kharif demonstrates the strongest overall agricultural performance among the three seasons.

* Highest average yield
* Highest water efficiency
* Highest average profit
* Lowest proportion of loss-making farms
* Highest rainfall availability

### Key Metrics

| Indicator         |            Kharif |
| ----------------- | ----------------: |
| Average Yield     |     **5.64 t/ha** |
| Median Yield      |     **1.95 t/ha** |
| Water Consumption |          6,094 m³ |
| Water Efficiency  | **5.91 t/1000m³** |
| Average Profit    |      **₹179,367** |
| Farms in Loss     |        **42.27%** |
| Rainfall          |      **885.6 mm** |
| Temperature       |            27.8°C |

---

## ⚠️ Zaid — Highest Resource & Financial Risk

Zaid presents the most challenging agricultural conditions.

Despite receiving the lowest rainfall, Zaid farms consume the **highest average amount of water** while achieving the **lowest water efficiency**.

| Indicator         |              Zaid |
| ----------------- | ----------------: |
| Average Yield     |         4.67 t/ha |
| Median Yield      |         1.45 t/ha |
| Water Consumption |      **6,423 m³** |
| Water Efficiency  | **4.44 t/1000m³** |
| Average Profit    |      **-₹26,592** |
| Farms in Loss     |        **64.52%** |
| Rainfall          |      **198.8 mm** |
| Temperature       |        **32.5°C** |

---

## ☀️ The Zaid Resource Paradox

```text
Lower Rainfall
      │
      ▼
Higher Irrigation Requirement
      │
      ▼
Higher Water Consumption
      │
      ▼
Lower Water Efficiency
      │
      ▼
Higher Operational Pressure
      │
      ▼
Lower Profitability
      │
      ▼
Higher Financial Risk
```

The findings indicate that Zaid requires greater dependence on irrigation while simultaneously experiencing weaker water productivity and financial outcomes.

---

# 📊 Seasonal Performance Comparison

| Indicator         |    🌧️ Kharif |      ❄️ Rabi |      ☀️ Zaid |
| ----------------- | ------------: | -----------: | -----------: |
| Yield             | **5.64 t/ha** |    5.08 t/ha |    4.67 t/ha |
| Median Yield      | **1.95 t/ha** |    1.66 t/ha |    1.45 t/ha |
| Water Consumption |      6,094 m³ | **5,837 m³** | **6,423 m³** |
| Water Efficiency  |      **5.91** |         5.18 |     **4.44** |
| Average Profit    |  **₹179,367** |      ₹88,197 | **-₹26,592** |
| Farms in Loss     |    **42.27%** |       51.28% |   **64.52%** |
| Rainfall          |  **885.6 mm** |     486.2 mm |     198.8 mm |
| Temperature       |        27.8°C |       22.4°C |   **32.5°C** |

---

# 🔬 Statistical Validation

Visual patterns were not treated as sufficient evidence.

Formal statistical methods were applied to determine whether observed seasonal differences were statistically meaningful.

## Distribution & Variance Diagnostics

```text
D'Agostino-Pearson Normality Test
              +
           Q-Q Plots
              +
         Levene's Test
              +
        Bartlett's Test
```

## Seasonal Comparison

```text
One-Way ANOVA
      │
      ├── Kruskal-Wallis
      │
      ├── Mann-Whitney U
      │
      └── Bonferroni Correction
```

## Interaction Analysis

```text
Season × State
      +
Season × Crop
      │
      ▼
Two-Way Factorial ANOVA
```

## Effect Size

The practical magnitude of observed differences is evaluated using:

* Eta-Squared
* Omega-Squared
* Cohen's d
* Hedges' g

---

# 🧪 Statistical Results

### Seasonal Yield Distribution

| Test             |                                            Result |
| ---------------- | ------------------------------------------------: |
| Kruskal-Wallis H |                                       **68.6043** |
| p-value          |                                 **1.267 × 10⁻¹⁵** |
| Interpretation   | **Statistically significant seasonal difference** |

The extremely small p-value provides strong evidence that yield distributions differ across seasons.

---

## 🔗 Interaction Effects

| Interaction    | F-statistic |          p-value | Interpretation                        |
| -------------- | ----------: | ---------------: | ------------------------------------- |
| Season × State |      1.6889 |           0.0511 | Not statistically significant at 0.05 |
| Season × Crop  | **19.4468** | **4.25 × 10⁻⁴⁸** | **Strong interaction**                |

### Key Interpretation

The **Season × Crop interaction** indicates that the impact of season on agricultural productivity depends substantially on the crop being cultivated.

Therefore:

> **Seasonal planning should not be based on season alone. Crop selection must also be considered.**

---

# 🧠 Analytical Framework

```text
                    ┌─────────────────────┐
                    │  Agricultural Data  │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Data Quality Checks  │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Data Preprocessing   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Feature Engineering │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Exploratory Analysis│
                    └──────────┬──────────┘
                               │
                               ▼
              ┌────────────────────────────────┐
              │ Seasonal Performance Analysis  │
              └───────────────┬────────────────┘
                              │
                              ▼
              ┌────────────────────────────────┐
              │ Correlation & Regression       │
              └───────────────┬────────────────┘
                              │
                              ▼
              ┌────────────────────────────────┐
              │ State & Crop Interaction       │
              └───────────────┬────────────────┘
                              │
                              ▼
              ┌────────────────────────────────┐
              │ Statistical Validation         │
              └───────────────┬────────────────┘
                              │
                              ▼
              ┌────────────────────────────────┐
              │ Outlier & Anomaly Detection   │
              └───────────────┬────────────────┘
                              │
                              ▼
                    ┌─────────────────────┐
                    │ Insights & Actions  │
                    └─────────────────────┘
```

---

# ⚙️ Data Preparation

The preprocessing pipeline includes:

* Missing-value treatment
* Categorical value normalization
* Data-quality validation
* Ground-truth consistency checks
* Duplicate and invalid-record checks
* Target leakage prevention
* Domain-specific feature construction

---

# 🧮 Feature Engineering

Several analytical features were derived to improve interpretation.

| Feature                      | Purpose                                      |
| ---------------------------- | -------------------------------------------- |
| `Profit_Margin_pct`          | Measures profitability relative to revenue   |
| `Verified_Land_Productivity` | Normalizes agricultural productivity by land |
| `Total_NPK_kg_ha`            | Represents combined fertilizer application   |

These engineered variables allow agricultural performance to be compared more meaningfully across farms.

---

# 📐 Relationship Analysis

The project investigates relationships between agricultural outcomes and explanatory variables including:

### Environmental Factors

* Rainfall
* Temperature
* Humidity
* Sunlight
* Soil pH

### Agricultural Inputs

* Water consumption
* Irrigation
* Nitrogen
* Phosphorus
* Potassium
* Pesticides

### Economic Variables

* Expenditure
* Revenue
* Profit
* Profit margin

The analysis considers both **linear and non-linear relationships** to identify potential saturation and diminishing-return effects.

---

# 🚨 Anomaly Detection

Unusual agricultural observations are identified using multiple complementary approaches.

### Detection Methods

```text
             ┌──────────────┐
             │   Tukey IQR  │
             └──────┬───────┘
                    │
             ┌──────▼───────┐
             │ Modified     │
             │ Z-Score      │
             └──────┬───────┘
                    │
             ┌──────▼───────┐
             │ Resource     │
             │ Thresholds   │
             └──────┬───────┘
                    │
             ┌──────▼───────┐
             │ Financial    │
             │ Loss Profile │
             └──────────────┘
```

### Focus Areas

* Extreme water consumption
* Loss-making farms
* Irrigation inefficiency
* Soil-related anomalies
* District-level deviations
* High-input farming conditions

---

# 💡 Evidence-Based Recommendations

## 1. 🌾 Optimize Zaid Crop Planning

Reduce dependence on highly water-intensive crops during Zaid where agricultural conditions make irrigation economically challenging.

Consider:

* Drought-tolerant crops
* Short-duration crops
* Higher-margin alternatives
* Crop-specific seasonal planning

---

## 2. 💧 Improve Water Efficiency

Water-stressed regions can benefit from efficient irrigation practices such as:

* Drip irrigation
* Sprinkler irrigation
* Irrigation scheduling
* Water-use monitoring

The objective is not simply to reduce water usage, but to **maximize output per unit of water consumed**.

---

## 3. 🧪 Adopt Precision Fertilization

The analysis indicates a potential plateau in returns beyond approximately **300 kg/ha Total NPK**.

This supports more targeted fertilizer application based on:

* Crop requirements
* Soil conditions
* Seasonal conditions
* Existing nutrient availability

---

## 4. 💰 Strengthen Financial Risk Assessment

Agricultural performance should not be evaluated using yield alone.

A more complete assessment should consider:

```text
Yield
  +
Revenue
  +
Input Cost
  +
Water Cost
  +
Operating Expenditure
  ↓
Profitability & Risk
```

---

# 🛠️ Technology Stack

<p align="center">

<img src="https://img.shields.io/badge/Python-3.9%2B-blue?logo=python">
<img src="https://img.shields.io/badge/Pandas-Data%20Processing-150458?logo=pandas">
<img src="https://img.shields.io/badge/NumPy-Numerical%20Computing-013243?logo=numpy">
<img src="https://img.shields.io/badge/SciPy-Statistical%20Analysis-8CAAE6">
<img src="https://img.shields.io/badge/Statsmodels-Statistical%20Modeling-4051B5">
<img src="https://img.shields.io/badge/Matplotlib-Visualization-orange">
<img src="https://img.shields.io/badge/Seaborn-Visualization-blue">
<img src="https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter">
<img src="https://img.shields.io/badge/Google%20Colab-Development-F9AB00?logo=googlecolab">

</p>

---

# 📂 Project Structure

```text
Seasonal-Agriculture-Performance-Analysis/
│
├── 📁 data/
│   └── seasonal_agriculture_performance_dataset.csv
│
├── 📁 notebooks/
│   └── Seasonal_Agriculture_Performance_Analysis.ipynb
│
├── 📁 outputs/
│   ├── figures/
│   ├── statistical_results/
│   └── tables/
│
├── 📁 reports/
│   └── project_report.pdf
│
├── 📄 README.md
├── 📄 requirements.txt
└── 📄 LICENSE
```

---

# 📓 Analysis Workflow

The complete notebook follows the sequence below:

```text
01. Environment Setup
02. Data Ingestion
03. Data Validation
04. Data Cleaning
05. Feature Engineering
06. Exploratory Data Analysis
07. Seasonal Comparison
08. Correlation Analysis
09. Regression Analysis
10. State & Crop Interaction
11. Statistical Testing
12. Outlier & Anomaly Detection
13. Insights
14. Recommendations
15. Conclusion
```

---

# 🚀 Reproducibility

## Requirements

```text
Python 3.9+
JupyterLab / Jupyter Notebook / Google Colab
```

## Installation

```bash
pip install pandas numpy scipy statsmodels matplotlib seaborn
```

## Reproducibility

A deterministic random seed of **42** is maintained wherever stochastic operations are used to ensure consistent analytical results across executions.

---

# ▶️ Getting Started

### 1. Clone the repository

```bash
git clone <repository-url>
cd Seasonal-Agriculture-Performance-Analysis
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Launch the notebook

```bash
jupyter notebook
```

### 4. Execute the analysis

Open the notebook inside the `notebooks/` directory and execute the cells sequentially.

---

# 📌 Key Takeaways

### 🌧️ Kharif

**Highest overall productivity and profitability**

### ❄️ Rabi

**Moderate performance with intermediate resource and financial outcomes**

### ☀️ Zaid

**Highest water demand, lowest water efficiency, and greatest financial risk**

### 🌱 Crop Selection

**Strongly influences how seasonal conditions translate into agricultural productivity**

### 🗺️ Regional Effects

**Seasonal behavior is comparatively consistent across states**

---

# 🏁 Conclusion

The analysis demonstrates that **seasonality is an important determinant of agricultural performance**, but it does not operate independently.

Kharif exhibits the strongest overall performance, while Zaid experiences the greatest combination of **water stress, reduced water efficiency, and financial risk**.

Most importantly, the statistically significant **Season × Crop interaction** demonstrates that agricultural outcomes depend on the combination of **when a crop is cultivated and which crop is selected**.

Therefore, effective agricultural planning should integrate:

> **Season + Crop + Environment + Resource Efficiency + Financial Performance**

This project provides a statistical and analytical framework for converting agricultural data into **evidence-based decisions for seasonal crop and resource planning**.

---

# 🌱 Project Impact

```text
Raw Agricultural Data
        ↓
Data Quality
        ↓
Analytical Features
        ↓
Statistical Evidence
        ↓
Seasonal Intelligence
        ↓
Agricultural Recommendations
        ↓
Evidence-Based Decisions
```

> **From Agricultural Data to Evidence-Based Decisions.**

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 👨‍💻 Project Information

**Program:** VOIS AICTE Batch 1
**Project:** Major Project
**Academic Year:** 2026–2027
**Domain:** Data Analytics & Agricultural Intelligence

---

<p align="center">
  <b>🌾 Seasonal Agriculture Performance Analysis</b><br>
  Data Analytics • Statistical Modeling • Agricultural Intelligence
</p>

<p align="center">
  ⭐ If you find this project useful, consider giving the repository a star.
</p>

