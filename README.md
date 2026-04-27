# Kyrgyzstan Education Statistics — Project

Statistical analysis of official education data published by the  
**National Statistics Committee of the Kyrgyz Republic**.


## Research Questions

1. How has population literacy evolved across census years (1989–2022)?
2. What is the trend in international student enrollment, and do CIS vs. non-CIS countries show different patterns?
3. Is there a significant correlation between the education budget and international enrollment?
4. How is the education budget distributed across sub-sectors?
5. Is the growth in non-CIS students significantly different from CIS students?
6. What are plausible enrollment and budget forecasts for 2025–2030?

---

## How to Run

### Prerequisites

```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn statsmodels
```

### Run order

Run notebooks in this order — each is self-contained but they share the same CSV inputs:

```
1. kyrgyzstan_education_analysis.ipynb   ← Start here (full pipeline)
2. kyrgyzstan_stats_only.ipynb           ← Statistics deep-dive
3. kyrgyzstan_visualisations.ipynb       ← All charts
4. kyrgyzstan_forecasting.ipynb          ← Forecasts
5. kyrgyzstan_report.ipynb               ← Final report (read-only summary)
```

All notebooks assume the four CSV files are in the **same directory** as the notebook files.

```bash
# From the project root
jupyter notebook
# or
jupyter lab
```

---

## Data Sources

All data is sourced from the **National Statistics Committee of the Kyrgyz Republic**  
(Нацстатком КР / Улуттук Статистика Комитети):  
https://www.stat.kg

Datasets are trilingual: Kyrgyz · Russian · English.

---

## Key Findings (Summary)

| Dimension | Finding |
|---|---|
| Literacy | Higher education tripled 1989–2022; illiteracy fell ~75% |
| CIS students | Peaked at 57,103 (2021), declining post-COVID to 25,073 (2024) |
| Non-CIS students | Grew continuously; now near-parity with CIS at 24,480 (2024) |
| Top origins (2024) | Uzbekistan 38%, India 25%, Pakistan 18% |
| Budget | 29× growth from 2001 to 2024; CAGR ≈ 15.3% |
| Correlation | Pearson r = 0.87–0.97 between budget and enrollment |
| Forecast (2030) | ARIMA: ~88K–93K total students; budget ~85–129K mln som (range by model) |
