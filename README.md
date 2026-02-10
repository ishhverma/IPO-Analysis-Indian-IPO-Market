# 📌 Indian IPO Market Analysis (EDA & Insights)
This repository contains a comprehensive exploratory data analysis (EDA) of the **Indian IPO market**. The analysis investigates IPO subscription trends, listing gains, and factors influencing IPO profitability.

## 🚀 Project Overview
Initial public offerings (IPOs) are a major event in financial markets, providing companies with a chance to raise capital and investors with early access to growth opportunities. This project analyzes historical IPO data to understand:
* What drives IPO listing gains?
* How do subscription rates affect profitability?
* Are there time-based trends in IPO performance?
* What are the key predictors of IPO success?

## 📁 Dataset Description
The dataset contains **319 IPO records** with the following columns:
| Column                  | Description                           |
| ----------------------- | ------------------------------------- |
| `Date`                  | IPO listing date                      |
| `IPOName`               | Name of the IPO                       |
| `Issue_Size`            | Issue size in crores                  |
| `Subscription_QIB`      | Subscription rate by QIB investors    |
| `Subscription_HNI`      | Subscription rate by HNI investors    |
| `Subscription_RII`      | Subscription rate by retail investors |
| `Subscription_Total`    | Total subscription rate               |
| `Issue_Price`           | IPO issue price                       |
| `Listing_Gains_Percent` | Percentage gain/loss on listing       |

## 📌 Key Findings & Insights
### ✔ Dataset Summary
* **319 IPOs**
* **9 columns**
* **No missing values**

### 🎯 Target Variable (Profitability)
A binary variable was created:
* `Listing_Gains_Profit = 1` → Profitable IPO (`Listing_Gains_Percent` > 0)
* `Listing_Gains_Profit = 0` → Non-profitable IPO

**Distribution:**
| Category       | Count | Percentage |
| -------------- | ----- | ---------- |
| Profitable     | 174   | 54.55%     |
| Non-profitable | 145   | 45.45%     |

### 📈 Listing Gains Statistics
| Metric  | Value   |
| ------- | ------- |
| Mean    | 4.74%   |
| Median  | 1.81%   |
| Std Dev | 47.65%  |
| Min     | -97.15% |
| Max     | 270.40% |
**Insight:** IPO listing gains are highly volatile, with large potential losses and gains.

### 📊 Subscription Metrics & Profitability
Higher subscription rates strongly correlate with profitability.
**Mean subscription by profitability:**
| Subscription Type | Non-profitable | Profitable |
| ----------------- | -------------- | ---------- |
| QIB               | 11.28          | 37.69      |
| HNI               | 27.73          | 105.39     |
| RII               | 4.74           | 11.75      |
| Total             | 12.33          | 40.04      |

### 🔗 Correlation with Listing Gains
| Feature            | Correlation |
| ------------------ | ----------- |
| Subscription_Total | 0.44        |
| Subscription_HNI   | 0.43        |
| Subscription_QIB   | 0.38        |
| Subscription_RII   | 0.32        |
| Issue_Size         | -0.10       |
| Issue_Price        | 0.05        |
**Insight:** Subscription metrics show moderate positive correlation with listing gains.

## 📆 Time Series & Trend Analysis
### Key Observations:
* Early years (2010–2011) show **negative listing gains**
* Later years show **positive gains**
* Quarterly trends show market volatility and changing investor sentiment

## 🧠 Subscription Tier Analysis
`Subscription_Total` was divided into three tiers:
| Tier   | Range      | Count |
| ------ | ---------- | ----- |
| Low    | ≤ 1.65     | 80    |
| Medium | 1.65–33.39 | 159   |
| High   | > 33.39    | 80    |

### Performance by Tier
| Tier   | Profitability (%) | Avg Listing Gains |
| ------ | ----------------- | ----------------- |
| High   | **80.00%**        | **36.11%**        |
| Medium | 53.46%            | -3.98%            |
| Low    | 31.25%            | -9.28%            |
**Conclusion:** High subscription IPOs are more likely to be profitable.

## 📊 Dashboard Overview
A consolidated dashboard was created featuring 12 key plots, including:
* Distribution plots of subscription metrics
* Profitability comparison plots
* Correlation heatmap
* Time-series trends
* Subscription tier analysis
* <img width="2390" height="1841" alt="image" src="https://github.com/user-attachments/assets/e92a4877-d584-47f3-bb80-18686159f655" />

# 🔗 Acknowledgements
This analysis was performed using Python libraries such as:
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Plotly

