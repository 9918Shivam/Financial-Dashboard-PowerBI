# 📊 Financial Sales Dashboard — Power BI

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Excel](https://img.shields.io/badge/Microsoft%20Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)
![Data Analyst](https://img.shields.io/badge/Role-Data%20Analyst-blue?style=for-the-badge)

---

## 📌 Project Overview

This project presents an **interactive financial sales dashboard** built in Microsoft Power BI using a real-world financial dataset. The dashboard provides end-to-end visibility into sales performance across segments, countries, products, and time periods — enabling business stakeholders to make data-driven decisions at a glance.

This is the **data analyst equivalent of a live web app** — just as a web developer deploys a working website you can interact with, a data analyst publishes an interactive dashboard that stakeholders can explore, filter, and draw insights from in real time.

---

## 🔴 Live Dashboard Preview

> 📎 **[View the Live Dashboard on Power BI Service](#)** ← *(Replace `#` with your published Power BI link)*

> 📸 **Dashboard Screenshots** — see the `/screenshots` folder for full-resolution previews.

---

## 🗂️ Repository Structure

```
financial-dashboard-powerbi/
│
├── 📁 data/
│   └── Financial_Sample.xlsx          # Raw dataset (source data)
│
├── 📁 report/
│   └── Financial_Sample_Dashboard.pbix  # Power BI Desktop report file
│
├── 📁 screenshots/
│   ├── overview_page.png              # Dashboard overview screenshot
│   ├── profit_by_segment.png          # Segment breakdown visual
│   └── country_analysis.png          # Geographic analysis visual
│
├── 📁 insights/
│   └── key_findings.md                # Summary of business insights found
│
└── README.md                          # You are here
```

---

## 📁 What to Upload on GitHub (As a Data Analyst)

Just like a web developer uploads their HTML/CSS/JS code so others can see **how it was built**, here's what you upload as a data analyst:

| File | Why Upload It | Equivalent in Web Dev |
|---|---|---|
| `Financial_Sample.xlsx` | The raw data source — shows where the analysis starts | Source code / database |
| `Financial_Sample_Dashboard.pbix` | The actual Power BI report — others can open it in Power BI Desktop | The entire codebase |
| `screenshots/*.png` | Visual proof of the dashboard — what it looks like without needing Power BI installed | A deployed live website / demo |
| `insights/key_findings.md` | A written summary of what you discovered | Documentation / comments in code |
| `README.md` | Project description, how to use it, what tools were used | README in any code project |

> ⚠️ **Note:** The `.pbix` file is large and binary. GitHub handles files up to 100MB. If it exceeds that, use [Git LFS](https://git-lfs.github.com/) or upload to OneDrive/Google Drive and link it in the README.

---

## 📊 Dataset Description

**Source:** Microsoft Financial Sample Dataset  
**File:** `Financial_Sample.xlsx`  
**Rows:** ~700 sales transactions  
**Time Period:** 2013 – 2014

### Columns

| Column | Description |
|---|---|
| `Segment` | Customer segment (Government, Midmarket, Enterprise, Small Business, Channel Partners) |
| `Country` | Sales country (Canada, France, Germany, Mexico, USA) |
| `Product` | Product name (Paseo, VTT, Velo, Amarilla, Montana, Carretera) |
| `Discount Band` | Discount tier applied (None, Low, Medium, High) |
| `Units Sold` | Number of units sold per transaction |
| `Manufacturing Price` | Cost to manufacture per unit |
| `Sale Price` | Price sold per unit |
| `Gross Sales` | Total revenue before discounts |
| `Discounts` | Total discount value applied |
| `Sales` | Net revenue after discounts |
| `COGS` | Cost of Goods Sold |
| `Profit` | Net profit (Sales − COGS) |
| `Date` | Transaction date |
| `Month Name / Month Number` | Month breakdown |
| `Year` | Year of transaction (2013 or 2014) |

---

## 📈 Dashboard Features

The Power BI dashboard includes the following pages and visuals:

### 🔹 Page 1 — Sales Overview
- Total Sales, Total Profit, Total Units Sold (KPI Cards)
- Sales trend over time (Line Chart)
- Sales by Country (Map or Bar Chart)

### 🔹 Page 2 — Profitability Analysis
- Profit by Segment (Bar Chart)
- Profit Margin by Product (Column Chart)
- Gross Sales vs. Discounts (Clustered Visual)

### 🔹 Page 3 — Product & Segment Breakdown
- Units Sold by Product (Pie / Donut Chart)
- Revenue contribution by Segment (Treemap)
- Discount Band impact on Profit (Matrix/Table)

### 🔹 Interactive Filters (Slicers)
- Filter by Year (2013 / 2014)
- Filter by Country
- Filter by Segment
- Filter by Product

---

## 💡 Key Business Insights

Here are the top findings from the analysis:

1. **Government segment** is the highest revenue-generating segment, but **Channel Partners** consistently achieve the highest profit margins.
2. **Paseo** is the top-selling product by units, while **Amarilla** and **VTT** drive the highest gross sales in certain markets.
3. **France and Germany** are the top-performing countries by both sales volume and profit.
4. **High discount bands significantly erode profit margins** — transactions with "High" discounts often result in near-zero or negative profit.
5. **2014 showed strong YoY growth** compared to 2013 across most segments and countries.

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Microsoft Power BI Desktop** | Dashboard design and data modelling |
| **Microsoft Excel** | Source data storage and initial exploration |
| **DAX (Data Analysis Expressions)** | Custom measures (Profit Margin %, YoY Growth, etc.) |
| **Power Query (M Language)** | Data cleaning and transformation |

---

## 🚀 How to Use This Project

### Option 1 — View the Live Dashboard (Recommended)
Click the published Power BI link at the top of this README. No installation needed.

### Option 2 — Open in Power BI Desktop
1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
2. Clone or download this repository
3. Open `report/Financial_Sample_Dashboard.pbix` in Power BI Desktop
4. Explore all pages, visuals, and slicers interactively

### Option 3 — Explore the Raw Data
Open `data/Financial_Sample.xlsx` in Microsoft Excel or Google Sheets to explore the underlying dataset directly.

---

## 📐 DAX Measures Used

```dax
-- Total Profit
Total Profit = SUM('Financials'[Profit])

-- Profit Margin %
Profit Margin % = DIVIDE([Total Profit], SUM('Financials'[Sales]), 0)

-- Total Sales
Total Sales = SUM('Financials'[ Sales])

-- YoY Sales Growth
YoY Growth % = 
DIVIDE(
    [Total Sales] - CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Financials'[Date])),
    CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Financials'[Date])),
    0
)
```

---

## 🖼️ Screenshots

| Overview | Profitability |
|---|---|
| *(Add screenshot here)* | *(Add screenshot here)* |

> 📌 **How to add screenshots:** Export visuals from Power BI → File → Export → Export to PNG/PDF, save to the `/screenshots` folder and link them above.

---

## 📬 Contact

**Your Name**  
📧 your.email@example.com  
🔗 [LinkedIn](#) | [Portfolio](#)

---

## 📄 License

This project uses the **Microsoft Financial Sample Dataset**, which is publicly available for educational and demonstration purposes.

---

> ⭐ If you found this project useful or insightful, please consider giving it a star on GitHub!
