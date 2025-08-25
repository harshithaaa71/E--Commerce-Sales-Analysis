# 📊 E-commerce Sales Analysis (Python + Power BI)

## Overview
Analyze global e-commerce sales to uncover revenue trends, top products/countries, and customer behavior.
Pipeline: **Python (Pandas) → Clean CSV → Power BI (Interactive Dashboard)**.

## Project Structure
E-commerce DA project/
├─ data/
│ ├─ raw/
│ └─ processed/
├─ notebook/
│ ├─ 01_ecommerce_eda.ipynb
│ └─ 02_analysis.ipynb
├─ dashboard/
│ ├─ E-commerce_Dashboard.pbix (optional / may be large)
│ └─ screenshots/
│ ├─ dashboard_main.png
│ ├─ revenue_by_country.png
│ └─ monthly_sales_trend.png
├─ README.md
└─ requirements.txt


## Key Measures (Power BI)
```DAX
Total Revenue = SUM('online_retail_cleaned'[total_price])
Total Orders = DISTINCTCOUNT('online_retail_cleaned'[invoice_id])
Total Customers = DISTINCTCOUNT('online_retail_cleaned'[customer_id])
AOV = DIVIDE([Total Revenue], [Total Orders])
---

## 2) “Invalid notebook” on GitHub → likely too big / outputs embedded
GitHub struggles to render notebooks that are large or saved with tons of embedded outputs. Fix it by clearing outputs and re-saving.

**In VS Code (open your .ipynb):**
1. **Kernel → Restart & Clear All Outputs** (or right-click in the notebook → *Clear All Outputs*).
2. Save the notebook (file size should drop a lot).
3. Commit & push:
   ```powershell
   git add notebook/01_ecommerce_eda.ipynb
   git commit -m "Clear outputs to fix GitHub rendering"
   git push
