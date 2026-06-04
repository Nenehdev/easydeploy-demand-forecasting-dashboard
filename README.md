# ⚡ EasyDeploy Demand Forecasting Dashboard

## Overview
![Performance Overview](dashboard_page1.png)
![Error & Dimension Analysis](dashboard_page2.png)
This is an interactive demand forecasting dashboard built in Microsoft 
Power BI using real data processed through the EasyDeploy AI platform. 
The dashboard visualizes model performance, forecast accuracy, and demand 
patterns across 10 stores and 50 items.

## Dashboard Pages

### Page 1 — Performance Overview
The executive summary page. Shows overall model performance at a glance.
- **5 KPI Cards** — Forecast Accuracy (92.37%), MAPE (7.63%), Total Actual 
  Demand (39.82M), Over-Forecast Rate (50.5%), Peak Period Demand (7.46M)
- **Actual vs Prediction Line Chart** — Two clean lines showing how closely 
  EasyDeploy's predictions track real demand across all 12 months
- **Forecast Error % by Month** — Color-coded bar chart showing which months 
  had high , moderate , or low forecast error
- **Interactive Slicers** — Filter by Store and Quarter to explore any 
  subset of the data

### Page 2 — Error & Dimension Analysis
The analyst deep dive page. Shows where the model performs well and where 
it needs attention.
- **Demand Breakdown by Dimension** — Toggle between Store and Item view 
  with a single slicer click. Color coded by performance level
- **Residual Error Heatmap** — Store × Month grid showing over-forecast 
  (red), perfect prediction (white), and under-forecast (blue) at a glance

## Key Findings
- EasyDeploy model achieved **92.37% forecast accuracy** across all stores 
  and items
- **MAPE of 7.63%** — predictions are typically within 8 units per 100, 
  well within industry standard range of 85-95%
- **Perfectly balanced bias** — 50.5% over-forecast rate indicates no 
  systematic directional error in the model
- **February and December** show the highest error rates — consistent with 
  known forecasting challenges around post-holiday and late-holiday demand
- **Peak season (Nov/Dec/Jan)** accounts for 19% of all annual demand — 
  critical planning window for inventory management

## Data Sources
| File | Description |
|---|---|
| `demand_train_sampled.csv` | Training data used to build the EasyDeploy model |
| `demand_test_with_actuals.csv` | Test dataset with real demand values |
| `inventory_demand_predictions.csv` | Predictions returned by EasyDeploy platform |

All data processed and structured using Python. Final dataset contains 
6,000 rows aggregated to one row per Store + Item + Month.

## Tools Used
- **Microsoft Power BI Desktop** — Dashboard design and visualization
- **Python (pandas, openpyxl)** — Data cleaning, aggregation and Excel generation
- **EasyDeploy AI** — Regression model training and prediction generation
- **Microsoft Excel** — Data staging for Power BI

## How to Open the Dashboard
1. Download **Power BI Desktop** free from microsoft.com
2. Download the `.pbix` file from this repository
3. Open it in Power BI Desktop
4. All data is pre-loaded — no additional setup needed
5. Use the Store and Quarter slicers to explore the data interactively

## EasyDeploy Platform
This dashboard was built to showcase output from the EasyDeploy AI 
platform. Learn more at [easydeploy.ai](https://www.easydeploy.ai)
