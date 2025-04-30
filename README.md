# 🌍 FDI, GDP Growth, and Governance: A Panel + Machine Learning Analysis

## 📘 Project Summary
This project investigates how the economic effect of **Foreign Direct Investment (FDI)** on **GDP growth** varies across countries depending on the quality of governance—specifically, **political stability** and **corruption**. By combining **panel regression** and **interpretable machine learning (XGBoost with SHAP)**, the project reveals how governance moderates the growth impact of FDI over time.

You can view the website here: [https://timothym4r.github.io/Politics-and-Corruption-on-FDI-GDP-relation/](https://timothym4r.github.io/Politics-and-Corruption-on-FDI-GDP-relation/)
---

## 🧩 Dataset Overview

- **Macroeconomic Variables:**  
  - `GDP Growth (%)`, `FDI (% of GDP)`, `Inflation (%)`, `Unemployment (%)`, `Trade Balance (% of GDP)`  
  - Source: [World Bank API](https://data.worldbank.org)

- **Governance Indicators:**  
  - `Political Stability`, `Control of Corruption`  
  - Source: [Worldwide Governance Indicators (WGI)](https://info.worldbank.org/governance/wgi/)

- **Coverage:**  
  - Years: 2000–2023  
  - Countries: ~120  
  - Format: **Balanced panel data**

---

## 🔧 Methodology

### 📊 Data Processing
- Harmonized country and year entries between datasets  
- Filled missing values using forward/backward fill and interpolation  
- Clipped extreme outliers at the 1st and 99th percentiles  
- Created interaction terms (FDI × governance scores)

### 🔍 Modeling

#### 📘 1. Panel Regression
- Fixed-effects model with country-level controls  
- Interaction terms for FDI × political stability and FDI × corruption  
- Diagnostic tests:  
  - Hausman test (justified fixed effects)  
  - Breusch-Pagan test (checked heteroskedasticity)

#### 🤖 2. XGBoost + SHAP
- Trained XGBoost model on full dataset  
- Interpreted feature and interaction effects using SHAP summary and interaction plots  
- Evaluated model fit using R² and RMSE  
  - Example: `R² = 0.406`, `RMSE = 3.031`

---

## 💡 Key Findings

- **FDI has a generally positive effect** on GDP growth across countries.
- The effect of FDI is **stronger in politically unstable environments**, suggesting that FDI may fill institutional or investment gaps in fragile states.
- **Corruption does not significantly alter** the relationship between FDI and growth, though mild patterns are visible.
- Panel regression and SHAP interaction plots **converge on the same conclusion** regarding political stability as a moderator.

---

## 📎 Deliverables

- Final cleaned dataset (`.csv`)  
- Jupyter notebooks for:
  - Data wrangling  
  - Panel regression  
  - XGBoost training and SHAP interpretation  
- Final report (LaTeX/PDF)  
- Visualizations:  
  - SHAP summary + interaction plots  
  - Partial Dependence Plots (PDPs)  
  - Regression coefficient table

---

## 🛠️ Tools and Libraries

- **Python**: `pandas`, `statsmodels`, `xgboost`, `shap`, `matplotlib`, `seaborn`, `scikit-learn`  
- **Statistical Tests**: Hausman test, Breusch-Pagan test  
- **LaTeX** (for final report formatting)

---

## 🔄 Limitations and Future Work

- Governance scores are perception-based and may lag behind reality  
- No causal identification strategy was used (e.g., IV, DiD)  
- Future work could incorporate:
  - Sector-specific FDI  
  - Time-varying institutional effects  
  - Firm-level or subnational data
