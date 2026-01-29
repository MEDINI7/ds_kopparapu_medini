# Trader Behavior vs Market Sentiment

This project is analyzes how trader performance changes with market sentiment (Fear vs Greed) using real trading data.

I used:
- Bitcoin Fear & Greed Index data  
- Historical trader data from Hyperliquid  

The main goal was to see:
- How profits and losses change in Fear vs Greed markets  
- Whether traders take more risk in Greed  
- How trade outcomes are distributed in different sentiment phases  

---

## Folder Structure

```
ds_kopparapu_medini/
├── notebook_1.ipynb
├── ds_report.pdf
├── README.md
├── csv_files/
│   ├── historical_data.csv
│   ├── fear_greed_index.csv
│   ├── merged_data.csv
│   └── daily_metrics.csv
└── outputs/
    ├── pnl_distribution_by_sentiment_full.png
    ├── pnl_distribution_by_sentiment_zoomed.png
    ├── total_volume_by_sentiment.png
    ├── trade_outcome_buckets_by_sentiment.png
    ├── trade_percentage_by_sentiment.png 
    └── trade_size_by_sentiment.png


```

---

## Data Used

1. **Fear & Greed Index**
   - Contains date and market sentiment (Fear / Greed)

2. **Historical Trader Data (Hyperliquid)**
   - Contains trades with fields like account, symbol, execution price, trade size (USD), timestamps, and closed PnL.

---

## What I Did

- Cleaned both datasets  
- Converted timestamps to dates  
- Merged trading data with sentiment data using date  
- Analyzed:
  - PnL distribution in Fear vs Greed
  - Trade counts in each sentiment
  - Trade volume by sentiment (total USD traded)
  - Trade size as a proxy for risk / leverage
  - Trade outcome buckets (loss, small win, big win, etc.)
  - Daily aggregated performance metrics
- Created plots for all important observations  
- Saved:
  - Processed datasets in `csv_files/`  
  - All plots in `outputs/`  

---

## How to Run

Open `notebook_1.ipynb` in Google Colab or Jupyter and run all cells.

The notebook:
- Loads data from `csv_files/`  
- Recreates the merged dataset  
- Recomputes daily metrics  
- Regenerates all plots in `outputs/`  

---

## Outputs

All important plots are saved in the `outputs/` folder, including:
- PnL distribution by sentiment (full and zoomed)  
- Percentage of trades in Fear vs Greed  
- Trade outcome bucket distribution by sentiment  

---

## Final Report

All findings and explanations are summarized in:

**`ds_report.pdf`**

---

## Main Observations

- Trading behavior clearly changes between Fear and Greed periods
- Fear periods have the highest trading volume and largest position sizes
- Greed periods show higher risk and more extreme profits and losses
- Trade size increases significantly during Fear and Greed, indicating higher risk-taking
- Trade outcome distributions are different in both regimes
- Detailed explanation is in the PDF report.

---



## Final Note

This project focuses more on:
- Clear analysis  
- Clean structure  
- Reproducibility  
- Practical insights  
