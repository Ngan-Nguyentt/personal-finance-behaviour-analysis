# Personal Finance Behaviour — Why the 50/30/20 Rule Fails

A statistical deep-dive into personal-finance behaviour that asks one practical question:
**why do most people fail to stay within budget, and what can they realistically do about it?**
The analysis validates spending, saving, and income patterns across ~5 years of data and informed
**SmartSpend**, a budgeting concept that classifies spending against the 50/30/20 rule in real time.

> Course: `CST2101 — Business Intelligence Programming` · Algonquin College · April 2026

---

## 🎯 Objectives
1. **50/30/20 compliance** — classify spending into Needs / Wants / Savings and measure how often users meet the rule.
2. **Budget-gap analysis** — how often, by how much, and in which categories users overspend.
3. **Future allocation** — savings, investment, and emergency-fund behaviour vs. goals.
4. **Income-segmented analysis & anomaly detection** — income quartiles plus z-score flags for unusual months.
5. **Visualisation & reporting** — 10 annotated charts that make the findings actionable.

## 🗂️ Dataset
**`personal-finance-dataset.csv`** — 3,000 anonymised records, 25 features, Jan 2019 – Nov 2023 (~5 years).
- **944 unique users** (user-month observations), 10 spending categories, 3 financial scenarios
  (normal 58% / inflation 22% / recession 20%), 3 income types (salary 72% / freelance 18% / mixed 11%).
- No missing values or duplicate rows — clean as supplied.

## 🔬 Methodology
| Step | What it does | Libraries |
|---|---|---|
| 1. Loading & EDA | schema validation, summary statistics | pandas, NumPy |
| 2. Needs vs. Wants | 50/30/20 mapping & compliance by scenario / income | pandas |
| 3. Over-budget alerts | budget-gap & category-overrun analysis | pandas, NumPy |
| 4. Future allocation | savings-goal achievement | pandas |
| 5. Income segments & anomalies | quartile segmentation, z-score flags | pandas, SciPy |
| 6. Visualisation | 10 charts with written interpretation | Matplotlib, Seaborn |

## 📈 Key findings
- 🚦 Only **22.3%** of records comply with 50/30/20 — the main culprit is **essential spending averaging
  ~60% of income** (well above the 50% target).
- 💸 **59.1%** of records exceed the user's own budget goal, with an **average overspend of ~$828**.
- 🐖 **Savings-goal achievement is below 12%** across all income types — a systemic, not individual, problem.
- 📊 Compliance climbs from **5.2% (lowest income quartile) to 43.5% (highest)** — the rule is structurally
  unrealistic for lower-income users.
- 🚨 **z-score anomaly detection** flags ~5% of records as statistically unusual spending months.

## 💡 Applied outcome — SmartSpend
The findings informed **SmartSpend**, a budgeting web-app concept (Django) that classifies spending against
the 50/30/20 rule in real time and warns users *before* they overspend. *(This repository contains the
analysis notebook and dataset; the notebook also documents the app design.)*

## 🛠️ Tech stack
`Python` · `pandas` · `NumPy` · `SciPy` · `Matplotlib` · `Seaborn` · `Jupyter` · `Django` (SmartSpend concept)

## 📁 Repository structure
```
personal-finance-analysis.ipynb   # full analysis notebook: EDA → statistics → insights
personal-finance-dataset.csv      # dataset (3,000 records, 25 features)
README.md
```

## ▶️ How to run
```bash
pip install pandas numpy scipy matplotlib seaborn jupyter
jupyter notebook personal-finance-analysis.ipynb
```

## 👥 Authors
Team project — **Ngan Nguyen** · **Duc Anh Ngo** · **DongHwan Won**
Business Intelligence Systems Infrastructure, Algonquin College

🔗 Portfolio: **https://ngan-nguyentt.github.io/**
