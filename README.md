# 🌍 FDI, GDP Growth, and Governance: A Panel Data Analysis

## 🚀 Project Overview
This project explores the relationship between **Foreign Direct Investment (FDI)** and **GDP growth** across countries, focusing on how **political stability** and **corruption** moderate this relationship.

### ✅ Key Details:
- **Goal:** Understand how governance quality influences the economic impact of FDI on GDP growth.  
- **Dataset:**  
   - Macroeconomic data from **World Bank API** (FDI, GDP growth, inflation, trade balance, unemployment)  
   - Governance indicators from **World Governance Indicators (WGI)** (political stability, corruption)  
- **Period:** 2000–2023  
- **Countries:** ~100+ countries  

---

## 📌 Phase 1 (Midterm) – Data Preparation and EDA
✔️ Data wrangling, merging, and cleaning  
✔️ Outlier handling using clipping (1st and 99th percentiles)  
✔️ Exploratory Data Analysis (EDA)  
   - Correlation matrix  
   - Distribution and scatter plots  
   - Interaction exploration (binned into categories)  
✔️ Multicollinearity check using VIF  

---

## 📌 Phase 2 (Final) – Panel Regression and Interpretation
🚧 **Baseline Model:** Fixed-effects panel regression to estimate FDI-GDP growth relationship  
🚧 **Interaction Terms:** Test moderating effect of political stability and corruption  
🚧 **Model Diagnostics:**  
- Breusch-Pagan test for heteroskedasticity  
- Hausman test for fixed vs random effects  

---

## 🔥 Challenges and Insights
- **Missing governance data for 2001** → Addressed using forward/backward fill  
- **High volatility** in governance scores → Smoothed using rolling averages  
- **No major multicollinearity detected** → Confirms model stability  

---
