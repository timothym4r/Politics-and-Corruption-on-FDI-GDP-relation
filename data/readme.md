# 📁 Data Sources and Loading Instructions

This folder contains all datasets used in the final project:  
**"The Relationship Between Foreign Direct Investment and Economic Growth: The Role of Political Stability and Corruption"**

---

## 📄 Files Included

### ✅ `merged_data.xlsx`
- **Description**: Final cleaned and merged dataset combining all relevant indicators across countries and years.
- **Source**: Generated locally from preprocessing scripts.
- **How to load**: Load directly from this repository.

---

### ✅ `missing_values.csv` and `missing_values.xlsx`
- **Description**: Intermediate files used for tracking and handling missing data.
- **Source**: Derived from raw merged datasets.
- **How to load**: Optional. Used during cleaning/debugging, but not essential for final analysis.

---

## 🌐 Online Data Sources

Some data were retrieved directly from **official APIs or sources**:

### 🔹 World Bank Development Indicators (WB API)
- **Indicators**:
  - Foreign Direct Investment (FDI) (% of GDP)
  - GDP Growth (%)
  - Inflation (%)
  - Trade Balance (% of GDP)
  - Unemployment (%)
- **Source**: [World Bank API](https://data.worldbank.org/)
- **How to load**: Recommend using `pandas.read_csv()` on a direct URL (e.g., `fread("https://data.worldbank.org/indicator/NY.GDP.MKTP.KD.ZG")`)  
  Alternatively, access the cleaned version from `merged_data.xlsx`.

---

### 🔹 Worldwide Governance Indicators (WGI)
- **Indicators**:
  - Political Stability
  - Control of Corruption
- **Source**: [Worldwide Governance Indicators](https://info.worldbank.org/governance/wgi/)
- **How to load**: Downloaded as `.xlsx` and merged into `merged_data.xlsx`

---