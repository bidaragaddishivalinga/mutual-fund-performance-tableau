# 📈 Institutional Mutual Fund Performance Analytics

## 🚀 Project Overview
This project transitions an exploratory data analysis (EDA) pipeline from Python into a production-ready, interactive Tableau BI dashboard. The objective is to analyze historical asset returns across dozens of fund categories to track risk profiles, isolate top alpha-generating individual assets, and visualize macroeconomic sector trends throughout 2024.

* **Interactive Live Dashboard:** [[Tableau Public URL]](https://public.tableau.com/app/profile/shivaling.bidaragaddi/viz/MutualFundPerformanceAnalyticsDashboard/Dashboard1?publish=yes)
* **Python Analysis Report:** [fund_performance_analysis.pdf](./fund_performance_analysis.pdf)
* **Processed Dataset:** [performance_summary.csv](./performance_summary.csv)

---

## 🛠️ Technical Implementation & Architecture

### 1. Programmatic Exploratory Data Analysis (Python)
* **Ingestion Pipelines:** Built data cleansing scripts using Python to normalize irregular, text-heavy date column schemas into structured temporal data types.
* **Feature Engineering:** Calculated categorical aggregate metrics and filtered outliers to export a high-density, performant `performance_summary.csv` matrix optimized for BI engines.

### 2. Executive BI Dashboard Architecture (Tableau)
The final interface leverages a standardized $2 \times 2$ analytical grid built on an automatic executive viewport configuration:
* **Category Performance Heatmap:** A high-level view showing month-over-month percentage returns across individual fund styles.
* **Top 10 Funds Performance:** Granular horizontal bar chart separating top-performing individual institutional assets.
* **Macro Market Trend Lines:** Line graphs tracking continuous rolling average momentum fluctuations.
* **Average Category Return:** Vertical distribution rankings to compare category baselines over late-year cycles.

### 📊 Calculation Logic & Interactivity
* **Aggregation Correction:** Configured foundational metrics using accurate statistical averages (`AVG`) rather than standard totals (`SUM`), preventing mathematical inflation of return percentages during broad category analysis.
* **Global Action Filters:** Deployed interactive funnel hooks across the master heatmap, allowing dynamic cross-filtering where clicking a specific asset tier automatically focuses all data quadrants on that category.
