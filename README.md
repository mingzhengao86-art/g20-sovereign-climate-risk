# G20 Sovereign Climate Risk Analysis

A data-driven analysis of carbon emissions trends, decoupling performance, and 2030 projections across G20 nations — framed through the lens of **sovereign climate risk**, a framework used by institutional investors to assess climate-related risks in government bonds and cross-border investments.

---

## Research Questions

1. Which countries are the largest emitters, and how have trends shifted since 1950?
2. Is there a statistically significant relationship between wealth (GDP per capita) and emissions intensity?
3. Which G20 countries have successfully decoupled economic growth from CO₂ emissions?
4. What do machine learning models project for G20 emissions in 2030?

---

## Repository Structure

```
g20-sovereign-climate-risk/
├── G20_Sovereign_Climate_Risk_Analysis.ipynb  # Main analysis notebook
├── Figure/                                     # All output visualizations
│   ├── fig1_top10_trends.png
│   ├── fig2_bubble.png
│   ├── fig3_regression.png
│   ├── fig4_structure.png
│   ├── fig5_g20_decoupling.png
│   ├── fig6_decoupling_scorecard.png
│   └── fig7_2030_projection_rf.png
└── Data/
    └── data_source.md                          # Data source documentation
```
---

## Key Findings

| Analysis | Finding |
|----------|---------|
| Historical trends | China surpassed the US around 2005; the US has declined ~20% since 2007 due to the shale gas revolution |
| Per-capita emissions | China emits 2.3× the US in total, yet only 55% per capita (8.2t vs 14.8t) |
| GDP–emissions correlation | Spearman r = 0.892 (p < 0.001); wealth strongly predicts emissions intensity |
| Fuel structure | China is ~70% coal-dependent; the US shifted significantly from coal to gas post-2008 |
| Decoupling leaders | UK (0.30), Germany (0.33), Russia (0.32) lead; Indonesia is the only non-decoupler |
| 2030 projection | Under BAU, India's emissions approach China's — the largest climate risk unknown |

---

## Methods

- **Statistical analysis:** Spearman correlation, log-linear regression (scipy)
- **Decoupling analysis:** GDP and CO₂ indexed to 1990 baseline across all G20 nations
- **Machine learning:** Random Forest vs. Linear Regression (scikit-learn), trained on 1990–2015, validated on 2016–2022
- **Projection scenario:** Business-as-usual (3% annual GDP growth, 1% population growth)

---

## Data Source

[Our World in Data — CO2 and Greenhouse Gas Emissions](https://github.com/owid/co2-data)  
Loaded directly via URL — no manual download required.

---

## Dependencies

```bash
pip install pandas numpy matplotlib scipy scikit-learn
```

---

## Author

**Mingzhen Gao**  
May 2026
