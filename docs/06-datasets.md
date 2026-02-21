# Datasets

[← Back to Index](../README.md) | [← Ontologies](05-ontologies.md) | [Next: Papers & Learning →](07-papers-learning.md)

---

<!-- 
💡 PLAIN ENGLISH: These are collections of real-world data you can use to 
train and test AI models. Some are free, some require registration, and 
some have strict rules about how you can use them.

⚠️ IMPORTANT: Always read the data use agreement (DUA) before using any 
dataset. Some explicitly prohibit sending data to cloud APIs.
-->

> **In simple terms:** Real data for training and testing AI models — but always check the rules before using them.

---

## Healthcare Datasets

| Dataset | Access | Description | Compliance Note |
|---------|--------|-------------|-----------------|
| **MIMIC-IV** | [physionet.org](https://physionet.org/content/mimiciv/) | De-identified ICU EHR data (2008-2019): vitals, labs, meds, notes, diagnoses. 40K+ patients. | ⚠️ Requires DUA. Do NOT send to cloud LLM APIs — local models only. |
| **MIMIC-CXR** | [physionet.org](https://physionet.org/content/mimic-cxr/) | 227,835 chest X-rays with de-identified radiology reports. | ⚠️ Same DUA. |
| **eICU Collaborative Research DB** | [physionet.org](https://physionet.org/content/eicu-crd/) | Multi-center ICU data from 200K+ stays. | Credentialed access required. |
| **MIMIC Code Repository** | [github.com/MIT-LCP/mimic-code](https://github.com/MIT-LCP/mimic-code) | SQL/Python code for MIMIC analysis; BigQuery and AWS available. | Open-source; data requires DUA. |
| **PhysioNet** | [physionet.org](https://physionet.org/) | ECG, EEG, waveform, vital sign datasets. | Varies by dataset. |
| **CheXpert (Stanford)** | [stanfordmlgroup.github.io](https://stanfordmlgroup.github.io/competitions/chexpert) | 224,316 chest X-rays with uncertainty labels. | Registration required. |
| **FAERS** | [fda.gov](https://www.fda.gov/drugs/drug-approvals-and-databases/fda-adverse-event-reporting-system-faers) | FDA adverse drug event reports — pharmacovigilance database. | Publicly available. |
| **ClinicalTrials.gov** | [clinicaltrials.gov](https://clinicaltrials.gov/) | 500K+ clinical trial records via API. | Publicly available. |

---

## Finance Datasets

| Dataset | Access | Description |
|---------|--------|-------------|
| **SEC EDGAR Full-Text** | [efts.sec.gov](https://efts.sec.gov/) | All SEC filings since 1993 — 10-K, 10-Q, 8-K, proxy statements. Free, public. |
| **FRED (St. Louis Fed)** | [fred.stlouisfed.org](https://fred.stlouisfed.org/) | 800K+ economic time series: GDP, inflation, employment, rates. Free API. |
| **Alpha Vantage** | [alphavantage.co](https://www.alphavantage.co/) | Stock quotes, indicators, fundamentals. Free tier with rate limits. |
| **OpenBB** | [github.com/OpenBB-finance/OpenBBTerminal](https://github.com/OpenBB-finance/OpenBBTerminal) | Aggregates 100+ financial data sources. Open-source. |
| **FinanceBench** | [github.com/patronus-ai/financebench](https://github.com/patronus-ai/financebench) | QA benchmark over real 10-K/10-Q filings. |
| **FinQA** | [github.com/czyssrs/FinQA](https://github.com/czyssrs/FinQA) | Expert-annotated numerical reasoning over financial reports. |
| **PIXIU / TiE** | [github.com/chancefocus/PIXIU](https://github.com/chancefocus/PIXIU) | Financial NLP benchmarks: sentiment, NER, QA, relation extraction. |

---

## Supply Chain Datasets

| Dataset | Access | Description |
|---------|--------|-------------|
| **M5 Forecasting (Walmart)** | [Kaggle](https://www.kaggle.com/c/m5-forecasting-accuracy) | 5 years Walmart sales; 42,840 time series. Gold standard for demand forecasting. |
| **Favorita Grocery Sales** | [Kaggle](https://www.kaggle.com/c/favorita-grocery-sales-forecasting) | Ecuadorian grocery sales with promotions, oil prices, holidays. |
| **UCI Supply Chain Datasets** | [archive.ics.uci.edu](https://archive.ics.uci.edu/) | Multiple SCM classification and regression datasets. |
| **Open Supply Hub** | [opensupplyhub.org](https://opensupplyhub.org/) | Global open database of supply chain facilities with standardized identifiers. |
| **US Freight Data** | [data.gov](https://www.data.gov/) | Government freight, shipping, and logistics datasets. |

---

## Data Use Agreement Warning

Several datasets listed here have strict data use agreements that **prohibit transmission to third-party cloud APIs**. This is especially true for:

- **MIMIC datasets** — PhysioNet requires credentialed access and prohibits cloud API usage
- **Any de-identified patient data** — Re-identification risk requires local processing
- **Proprietary financial data** — Licensing terms may restrict API transmission

**Always:**
1. Read the full DUA before downloading
2. Use local models when cloud transmission is prohibited
3. Document your compliance measures
4. Maintain audit trails for data access

---

[← Ontologies](05-ontologies.md) | [Next: Papers & Learning →](07-papers-learning.md)
