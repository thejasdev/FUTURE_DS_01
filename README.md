# 🛒 Supermarket Sales & Profitability Dashboard (Power BI)

An end-to-end data analytics project featuring a custom **Python (Pandas) ETL pipeline** and an interactive **Power BI dashboard**. This project transforms raw Superstore sales data into actionable business intelligence, helping stakeholders identify profit drivers, expose geographical financial leaks, and optimize supply chain logistics.

An interactive **Power BI dashboard** built using the **Superstore Sales Dataset** to analyze sales performance, profitability, customer segments, and regional trends. The dashboard helps businesses identify profit drivers, loss-making areas, and opportunities for growth through data-driven insights.

* **Project Type:** Data Analytics Dashboard
* **Tool:** Microsoft Power BI
* **Internship:** Future Interns – Data Science & Analytics Internship (Task 1)

---

## 📌 Project Overview 

Businesses generate massive amounts of transactional data, but raw data alone cannot dictate strategy. This project bridges the gap between raw data and executive decision-making. 

Instead of relying solely on frontend visualization tools, this project utilizes a robust **Python-based ETL (Extract, Transform, Load)** architecture to rigorously clean, validate, and engineer the data before it ever reaches Power BI. 

### Core Business Questions Answered
1. Which products and categories generate the most revenue vs. actual profit?
2. How do sales trend over time, and what is the seasonal impact?
3. Where are the geographical "financial leaks" (high sales, negative margin)?
4. Where should the business focus its marketing spend to grow faster?
5. How efficient is the current shipping and logistics pipeline?

---

## ⚙️ Phase 1: Python ETL Pipeline (Data Engineering)
The raw dataset was audited, cleaned, and enriched using a custom Jupyter Notebook pipeline (`ETL_Pipeline.ipynb`) before visualization.

### Data Cleaning & Transformation
* **Type Casting:** Resolved datetime parsing conflicts for `order_date` and `ship_date`.
* **String Formatting:** Fixed the "lost leading zeros" bug in `postal_code` by enforcing strict string casting.
* **Standardization:** Converted all column headers to `snake_case` for programmatic querying.
* **Validation:** Implemented an automated verification script to validate row counts and data types post-cleaning.

### Feature Engineering
New business logic was calculated directly in Python to empower the dashboard:
* `days_to_ship`: Calculated the exact logistics turnaround time (Ship Date - Order Date).
* `profit_margin`: Engineered the financial efficiency metric (Profit / Sales).
* `order_year` & `order_month_name`: Extracted date parts for advanced time-series analysis.

---

## 📂 Dataset Details
* **Source:** [Superstore Sales Dataset (Kaggle)](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)
* **Raw Data Shape:** 9,994 Rows | 21 Columns
* **Processed Data Shape:** 9,994 Rows | 25 Columns *(After engineering new features like profit_margin and days_to_ship)*

*Note: The dataset was lightweight enough (approx. 1.6 MB) to be version-controlled directly within this repository for seamless reproducibility.*

---

## 📊 Phase 2: Power BI Dashboard (Business Intelligence)
The fully processed dataset (`superstore_sales_clean.csv`) was ingested into Power BI to create a dynamic, F-pattern executive dashboard featuring a custom branded color theme.

### Executive KPIs
* 💰 **Total Revenue**
* 📈 **Total Profit**
* 📊 **Avg Profit Margin (%)**

### Visual Architecture
* **Sales & Profit Trend Over Time (Line Chart):** Year-over-year comparison highlighting Q4 seasonality.
* **Top Revenue Drivers (Horizontal Bar Chart):** Category performance sorted dynamically.
* **Profitability Leak Detection (Matrix):** Drill-down pivot table exposing negative margins at the regional level.
* **The Strategy Quadrant (Scatter Plot):** Risk vs. Reward mapping (Sales vs. Profit Margin) to identify "Goldmine" and "Danger" products.
* **Shipping Efficiency (Donut Chart):** Analyzing average `days_to_ship` by delivery mode.

### Interactive Features
* Dynamic cross-filtering across all visuals.
* Slicers for **Region**, **Year**, and **Customer Segment**.
* Custom DAX measures for dynamic calculations and conditional formatting.

---

### 💡 Key Insights & Business Recommendations

* **The Q4 Surge:** The business experiences extreme seasonality, with massive revenue spikes in November/December.
* **The Profitability Leak:** While overall sales are strong, the Matrix visual reveals that the *Furniture* category in the *Central Region* operates at a negative profit margin.
* **The Strategy Pivot:** The Scatter Plot reveals that Copiers and Accessories yield high sales AND high margins.
* **Logistics Waste:** Analysis of the engineered `days_to_ship` feature shows minimal turnaround difference between premium and standard shipping tiers.

---

# 💡 Business Recommendations

1. Reduce excessive discounts on Tables and Bookcases to improve profitability.
2. Increase marketing and inventory investment in Technology and Office Supplies.
3. Investigate operational challenges affecting the South region.
4. Monitor high-discount transactions and implement discount control policies.
5. Focus promotional campaigns on high-performing customer segments.

---

## 🛠️ Tools & Technologies
* **Data Analysis:** Python, Pandas, NumPy, Jupyter Notebook
* **Version Control:** Git, GitHub
* **Business Intelligence:** Power BI Desktop, DAX
* **Core Skills:** ETL, Data Cleaning, Feature Engineering, Data Modeling, Dashboard UI/UX Design, Analytical Thinking.

---

## 📁 Project Structure
```text
Supermarket-Sales-Dashboard/
│
├── data/
│   ├── raw/                 # Original uncleaned dataset
│   └── processed/           # superstore_sales_clean.csv (Ready for BI)
│
├── notebooks/
│   └── ETL_Pipeline.ipynb   # Python data engineering and cleaning code
│
├── dashboard.pbix           # Power BI interactive dashboard
├── .gitignore               # Version control configurations
├── README.md                # Project documentation
└── screenshots/
    └── dashboard_overview.png
```

# 📂 Dataset

**Source:** Superstore Sales Dataset (Kaggle)

https://www.kaggle.com/datasets/vivek468/superstore-dataset-final

---

# 🎯 Skills Demonstrated

* Data Cleaning
* Data Transformation
* Data Modeling
* KPI Development
* Business Intelligence
* Dashboard Design
* DAX
* Power Query
* Data Visualization
* Business Insight Generation
* Analytical Thinking

---

# 🚀 Future Improvements

* Add customer-level profitability analysis.
* Build forecasting using Power BI forecasting features.
* Create drill-through pages for detailed product analysis.
* Include dynamic tooltips and bookmarks.
* Publish the dashboard to the Power BI Service for online access.

---

# 🎓 About This Project

This project was completed as part of the Future Interns Data Science & Analytics Internship. The objective was to build a complete, professional-grade pipeline—moving beyond basic charting to demonstrate how rigorous data engineering directly fuels high-level business strategy.

The objective was to convert raw sales data into a professional, interactive business dashboard capable of supporting informed, data-driven decision-making.

---

👤 Connect with Me

💼 LinkedIn: (https://www.linkedin.com/in/thejasdev/)

---

## ⭐ If you found this project useful, consider giving this repository a star!
