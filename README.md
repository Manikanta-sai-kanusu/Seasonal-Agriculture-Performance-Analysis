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
