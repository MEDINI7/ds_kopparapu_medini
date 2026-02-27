# Trader Behavior vs Market Sentiment Analysis

This project analyzes how trader performance and behavior change across different market sentiment regimes (Fear, Greed, Extreme Fear, Extreme Greed, Neutral) using real-world trading data.

---

##  I used:

* Bitcoin Fear & Greed Index data
* Historical trader data from Hyperliquid

## The main goal was to see:

* How profits and losses change across sentiment regimes
* Whether trader behavior shifts during Fear and Greed
* How trader performance differs by activity and consistency
* How sentiment can inform smarter trading strategies

---

##  Folder Structure

```text
ds_kopparapu_medini/
├── notebook_1.ipynb       # Baseline trade-level sentiment analysis
├── notebook_2.ipynb       # Trader-level profiling and segmentation
├── ds_report.pdf          # Summary of insights and findings
├── README.md              # Project documentation
├── csv_files/             # Raw and processed datasets
│   ├── historical_data.csv
│   ├── fear_greed_index.csv
│   ├── merged_data.csv
│   └── daily_metrics.csv
└── outputs/               # Visualizations
    ├── pnl_distribution_by_sentiment_full.png
    ├── pnl_distribution_by_sentiment_zoomed.png
    ├── total_volume_by_sentiment.png
    ├── trade_outcome_buckets_by_sentiment.png
    ├── trade_percentage_by_sentiment.png 
    └── trade_size_by_sentiment.png
```
---
## Notebook Overview
### notebook_1.ipynb

### This notebook focuses on baseline trade-level sentiment analysis.
It includes:

* Data cleaning and preprocessing
* Timestamp conversion and daily alignment
* Merging trading and sentiment datasets
* PnL distribution analysis across sentiment regimes
* Trade counts and volume comparison
* Trade size as a proxy for risk
* Daily aggregated performance metrics

This provides exploratory insight into how sentiment correlates with trade outcomes.

---

### notebook_2.ipynb

### This notebook extends the analysis with trader-level behavioral profiling and segmentation.

It includes:

* Trader-level aggregation (total PnL, win rate, trade count, position size, volatility)
* Activity-based segmentation (Frequent vs Infrequent traders)
* Consistency-based segmentation (Consistent Winners vs Inconsistent Traders)
* Sentiment × Segment performance comparison
* Volatility analysis as a drawdown proxy
* Regime-based behavioral insights
* Actionable trading strategy recommendations

This notebook focuses on structured reasoning and translating analysis into practical strategy insights.

---

## Methodology
### Part A — Data Preparation

* Cleaned both datasets
* Converted timestamps to daily format
* Merged sentiment and trading data by date
* Created key metrics:
* Daily PnL per trader
* Win rate
* Trade count
* Average position size
* PnL volatility (risk proxy)

### Part B — Regime-Based Analysis

* Compared performance across Fear, Greed, Extreme, and Neutral regimes
* Evaluated differences in average PnL and win rate
* Measured volatility changes across regimes
* Analyzed behavioral shifts in trade frequency and position size
* Identified trader segments and compared regime-dependent performance

### Part C — Actionable Output

* Based on the findings, the following strategy rules were proposed:
* Dynamic capital allocation toward high-activity traders during strong sentiment regimes
* Stricter risk controls during fear periods due to elevated volatility
* Reduced trade frequency during neutral regimes to avoid overtrading
* Recognition that sentiment amplifies performance differences between consistent and inconsistent traders

---

## Key Observations

* Trader performance is highly regime-dependent
* Greed regimes generate higher average PnL
* Fear regimes significantly increase volatility and trading activity
* Neutral regimes reduce win rates and highlight skill differences
* Sentiment amplifies dispersion between high-skill and low-skill traders

 --- 

## How to Run

* Open either: notebook_1.ipynb or notebook_2.ipynb in Google Colab or Jupyter and run all cells.

### The notebooks:

* Load data from csv_files/
* Recreate merged datasets
* Recompute metrics
* Regenerate all analysis tables and plots

---

## Final Note

### This project emphasizes:
* Clean data alignment
* Structured analysis
* Regime-aware trader segmentation
* Actionable insights
* Reproducibility and clarity

 --- 

