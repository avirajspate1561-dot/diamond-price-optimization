# Diamond Price Optimization & Statistical Confidence Interval Analysis

A statistical data analytics capstone project examining pricing distributions, cut quality proportions, and confidence intervals across 5,000 diamond observations to support retail inventory and pricing strategies.

---

## Executive Summary

To optimize pricing strategies and maintain market competitiveness, this analysis models key statistical parameters for diamond pricing. Using $z$-score confidence interval modeling across sample populations, we establish lower and upper pricing bounds for overall inventory as well as specific cut categories (Premium vs. Fair). Additionally, inventory proportion estimates with 90% confidence intervals enable optimized purchasing forecasts.

### Key Performance Indicators & Summary Statistics
* **Total Sample Analyzed ($n$)**: 5,000 observations
* **Overall Average Price ($\bar{x}$)**: **$3,862.42** ($s = \$3,977.56$)
* **Premium Cut Average Price ($\bar{x}$)**: **$4,524.14** ($s = \$4,351.40$, $n = 1,305$)
* **Fair Cut Average Price ($\bar{x}$)**: **$4,333.56** ($s = \$3,277.94$, $n = 147$)
* **High-Demand Cuts ('Premium' or 'Ideal')**: **66.32%** of inventory ($n = 3,316$)

---

## Statistical Results & Confidence Intervals

### 1. Exercise 1 — Price Means & 95% Confidence Intervals ($z = 1.96$)

$$\text{Margin of Error (MoE)} = z \cdot \left(\frac{s}{\sqrt{n}}\right)$$

| Diamond Category | Sample Size ($n$) | Mean Price ($\bar{x}$) | Std Dev ($s$) | Margin of Error | 95% Confidence Interval |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **All Diamonds** | 5,000 | \$3,862.42 | \$3,977.56 | \$110.25 | **[\$3,752.16, \$3,972.67]** |
| **Premium Cut** | 1,305 | \$4,524.14 | \$4,351.40 | \$236.09 | **[\$4,288.05, \$4,760.24]** |
| **Fair Cut** | 147 | \$4,333.56 | \$3,277.94 | \$529.91 | **[\$3,803.65, \$4,863.46]** |

### 2. Exercise 2 — Cut Proportions & 90% Confidence Intervals ($z = 1.645$)

$$\text{MoE} = z \cdot \sqrt{\frac{\hat{p}(1 - \hat{p})}{n}}$$

| Cut Category | Count | Total ($n$) | Sample Proportion ($\hat{p}$) | Margin of Error | 90% Confidence Interval |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Premium or Ideal** | 3,316 | 5,000 | 0.6632 (66.32%) | 0.0110 (1.10%) | **[65.22%, 67.42%]** |
| **Fair Cut** | 147 | 5,000 | 0.0294 (2.94%) | 0.0039 (0.39%) | **[2.55%, 3.33%]** |

---

## Visualizations

<p align="center">
  <img src="visuals/price_ci_by_cut.png" alt="95% Confidence Intervals for Mean Diamond Price" width="48%"/>
  <img src="visuals/cut_proportion_ci.png" alt="Diamond Distribution by Cut Quality" width="48%"/>
</p>

---

## Business Insights & Strategy Recommendations

1. **Premium Cut Value Positioning**: Premium cut diamonds command the highest average price ($\$4,524.14$), significantly above the population mean. Pricing algorithms should account for the wider margin of error ($\pm \$236.09$) due to higher variability in carat sizes within this segment.
2. **Fair Cut Pricing Overhaul**: Fair cut diamonds exhibit a surprisingly high mean price ($\$4,333.56$), driven by larger average carat sizes despite poorer cut quality. Pricing strategy should isolate carat weight from cut quality to prevent overpricing lower-grade stones.
3. **Inventory Procurement Focus**: High-demand cuts ('Premium' and 'Ideal') account for over 66% of inventory. Stock allocation models should maintain minimum inventory thresholds between 65.22% and 67.42% to satisfy customer purchasing trends.

---

## Repository Structure

```text
diamond-price-optimization/
├── README.md                                     <- Executive summary & portfolio documentation
├── LICENSE                                       <- MIT License
├── data/
│   └── C2M3_GradedLab_Diamond_prices.xlsx       <- Dataset (5,000 records)
├── notebooks/
│   └── diamond_price_analysis.ipynb              <- Analytical notebook with CI modeling
└── visuals/
    ├── price_ci_by_cut.png                       <- 95% Confidence interval plot export
    └── cut_proportion_ci.png                    <- Cut distribution plot export
```

---

## Tools & Libraries Used

* **Python 3.10+**: Data processing and statistical computations
* **Pandas & NumPy**: Data manipulation and numerical operations
* **Matplotlib & Seaborn**: Visualization and plot exports
* **OpenPyXL**: Excel file reading with memory streaming
* **VS Code / Jupyter Notebook**: Interactive development environment
* **Git / GitHub**: Version control and portfolio hosting

---

## Author
* **GitHub Profile**: [@avirajspate1561-dot](https://github.com/avirajspate1561-dot)S