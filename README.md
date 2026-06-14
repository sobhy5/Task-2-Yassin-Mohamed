# Project 2: Exploratory Data Analysis (EDA)
**DecodeLabs Industrial Training | Batch 2026**

## Overview
This project performs a full EDA on the cleaned cafe sales dataset from Project 1. The goal is to uncover hidden patterns, trends, and outliers — transforming raw numbers into actionable business insights.

## Business Question
> What drives revenue at the cafe, and where are the growth opportunities?

## Dataset
- **Source**: cafe_sales_CLEAN.csv (output of Project 1)
- **Records**: 300 transactions | Jan–Dec 2023
- **Columns**: Transaction_ID, Date, Item, Category, Quantity, Price_Per_Unit, Total_Spent, Payment_Method

## Files
| File | Description |
|------|-------------|
| `cafe_sales_CLEAN.csv` | Input dataset (from Project 1) |
| `eda_notebook.ipynb` | Full EDA Jupyter notebook |
| `eda_report.pdf` | Executive summary PDF report |
| `eda_dashboard.png` | 6-chart EDA visualization dashboard |
| `eda_outliers.png` | Outlier detection charts (IQR method) |

## How to Run
1. Upload `cafe_sales_CLEAN.csv`, `eda_dashboard.png`, and `eda_outliers.png` to Colab Files panel
2. Open `eda_notebook.ipynb` in Google Colab
3. Run All Cells

## Analysis Performed
- Descriptive statistics (mean, median, std, five-number summary)
- Skewness analysis (Total_Spent = 0.818, right-skewed)
- Outlier detection using IQR method
- Monthly revenue trend analysis
- Item & category performance ranking
- Payment method breakdown
- Pearson correlation analysis

## Key Findings
1. **Food category = 56% of revenue** despite 47% of transactions
2. **Salad has highest avg order value** ($17.79) — prime upsell target
3. **Total_Spent is right-skewed** — median ($10.50) is a better central measure than mean ($11.79)
4. **4 outliers detected** — classified as SIGNAL (large group orders), not noise
5. **Strong correlation** between Quantity and Total_Spent (r = 0.80)
6. **Debit Card** users spend most per transaction ($12.44 avg)

## Tools
- Python 3
- pandas
- numpy
- matplotlib
- scipy

## Framework
IPO Model: Input (cleaned CSV) → Process (statistical analysis) → Output (insights + recommendations)
