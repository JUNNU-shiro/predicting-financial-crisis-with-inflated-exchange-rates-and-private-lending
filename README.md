# Predicting Financial Crisis with Inflated Exchange Rates and Private Lending

This repository hosts the research, data pipeline, and econometric modelling code for the Master's Thesis of **Varun Sai Bera** (EDHEC Business School, Class of 2025) under the supervision of **Prof. Arnaud Dufays**.  
It investigates how exchange-rate misalignments and private-sector credit expansions contribute to episodes of financial instability in India.

---

## 📘 Abstract

This thesis examines whether periods of inflated exchange rates and elevated private lending levels have contributed to financial instability in India between 2014 and 2024.  
The study employs **Vector Autoregression (VAR)** and **Markov-Switching VAR (MS-VAR)** models using official **Reserve Bank of India (RBI)** datasets on exchange rates, non-food credit, inflation, and interest rates.  

Empirical results show that:
- Credit expansions systematically precede rupee depreciation by 1–2 months.  
- Regime shifts detected through MS-VAR align closely with major stress episodes such as the **COVID-19 liquidity shock**.  
- Policy simulations indicate that counter-cyclical capital buffers and borrower-based limits could have mitigated instability.  

These insights inform early-warning frameworks for macroprudential policy in emerging economies.

## 🧠 Key Features
- **High-frequency RBI data (fortnightly, 2017–2025)** harmonized for exchange rate and private lending.
- **Rolling-window VAR** to detect evolving spill-over dynamics.
- **CUSUM stability tests** and **PELT break detection** to identify crisis-linked parameter shifts.
- **Visualization** of coefficient drift and regime transitions.

---

## ⚙️ Methodology Overview
| Step | Description |
|------|--------------|
| 1 | Data extraction from RBI Database on Indian Economy |
| 2 | Stationarity tests – ADF & KPSS |
| 3 | VAR(1) estimation and diagnostics |
| 4 | Rolling-window estimation to capture parameter drift |
| 5 | Structural break tests (CUSUM, MOSUM, sup-Wald) |
| 6 | Regime detection using PELT algorithm |
| 7 | MS-VAR extension (Markov-switching) |

---

## 📂 Repository Contents
| File | Description |
|------|-------------|
| `VAR_CUMSUM.ipynb` | Jupyter Notebook implementing the VAR + CUSUM pipeline |
| `VAR_CUMSUM.html.pdf` | Static export of the notebook for quick review |
| `THESIS_DRAFT.docx` | Full thesis document (EDHEC Master Thesis Template) |
| `README.md` | Project documentation (this file) |

---

## 🧰 Environment Setup
### Requirements
```bash
python==3.11
pandas==2.2
statsmodels==0.15
ruptures==1.1
matplotlib
numpy
