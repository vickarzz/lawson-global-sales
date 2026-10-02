# 🛒 Lawson Sales Summary Dashboard

End-to-end sales analytics solution for **Lawson**. The project consolidates transactional sales data through an ETL pipeline built with **SSIS, Python, and SQL**, and delivers an interactive **Power BI** dashboard that tracks profitability, revenue, and cost drivers across time, product categories, and regions.

![Lawson Sales Summary Dashboard](images/Lawson_Sales_Summary.png)

---

## 👤 My Role

- Gathered business requirements and defined sales and profitability KPIs
- Designed and built ETL workflows using **SSIS**
- Developed **Python** scripts for data cleansing and validation
- Built the data model and KPI logic in **SQL**
- Designed and developed the interactive **Power BI** dashboard
---

## 📌 Project Highlights

- **Single-page executive dashboard** summarizing sales performance at a glance
- **5 headline KPIs**: Profit, Revenue, Tax Amount, Unit Cost, and Freight Cost
- **End-to-end data pipeline**: ETL with SSIS, data cleansing with Python, and data modeling in SQL
- **6 interactive slicers** for flexible analysis: Year, Month, Item Name, Subcategory, Area, and Status
- **Geo-analytics** with a map view of performance across sales regions

---

## 🛠️ Tech Stack

| Layer | Tools | Purpose |
|---|---|---|
| Data Extraction & Loading | **SSIS** | Scheduled ETL packages to extract sales data and load it into the data warehouse |
| Data Processing | **Python** | Data cleansing, validation, and transformation before loading |
| Data Modeling & Querying | **SQL** | Staging, fact and dimension tables, and KPI calculation logic |
| Visualization | **Power BI** | Interactive dashboard with slicers, maps, and drill-down |

---

## 🏗️ Data Architecture

```
┌──────────────────────┐     ┌──────────────────┐     ┌──────────────────┐     ┌──────────────────┐
│   Source Data        │     │   ETL Layer      │     │  Data Warehouse  │     │  Presentation    │
│                      │     │                  │     │                  │     │                  │
│ • Sales transactions │ ──► │ • SSIS packages  │ ──► │ • SQL fact &     │ ──► │ • Power BI       │
│ • Product master     │     │ • Python scripts │     │   dimension      │     │   dashboard      │
│ • Region / area      │     │ • SQL staging    │     │   tables         │     │ • Slicers & map  │
└──────────────────────┘     └──────────────────┘     └──────────────────┘     └──────────────────┘
```

---

## 🎛️ Filters (Slicers)

| Slicer | Description |
|---|---|
| **Year** | Fiscal / calendar year of the transaction |
| **Month** | Month of the transaction |
| **Item Name** | Individual product |
| **Subcategory** | Product subcategory |
| **Area** | Sales region (e.g., Australia, Canada, Central, France, Germany, Northeast, Northwest, Southeast, Southwest) |
| **Status** | Order / transaction status |

---

## 📊 Dashboard Components

### 1. KPI Cards

Headline metrics that give an instant view of overall business performance:

| KPI | Description |
|---|---|
| **Profit** | Net profit after all costs |
| **Revenue** | Total sales value |
| **Tax Amount** | Total tax on sales |
| **Unit Cost** | Total product cost of goods sold |
| **Freight Cost** | Total shipping and logistics cost |

**KPI logic:** Profit = Revenue − Unit Cost − Tax Amount − Freight Cost

### 2. Profit by Month

Column chart showing the monthly profit trend from January to December.

**Business questions answered:** Which months drive the most profit? Are there seasonal peaks or slow periods that need promotion or inventory planning?

### 3. Top 5 Profit by Category

Pie chart showing the five most profitable product categories, with each category's profit value and share of total.

**Business questions answered:** Which categories contribute the most to profit? Is profit concentrated in a few categories or spread evenly?

### 4. Summary Maps

Map visual showing sales performance across all regions, color-coded by area.

**Business questions answered:** Which regions perform best? Where are the growth opportunities or underperforming markets?

### 5. Top 5 Profit by Area

Clustered bar chart comparing monthly profit across the top-performing areas.

**Business questions answered:** How do top regions compare month by month? Which region leads in each period?

---

## 💡 Key Insights

- **Profit margin** sits at roughly **36%** of revenue ($40.05M profit on $109.85M revenue)
- **Unit cost** is the largest cost driver, at over half of total revenue
- **Freight cost** is relatively small (under 3% of revenue), so logistics is not a major margin pressure
- **Monthly profit is uneven**: March is the strongest month, while February, April, and November are noticeably lower, pointing to clear seasonal patterns

---

## 🎯 Business Value

- **Executive visibility:** one page that summarizes profitability and cost structure
- **Cost control:** separates unit, tax, and freight costs to show where margin is lost
- **Product strategy:** identifies the most profitable categories to prioritize
- **Regional planning:** compares area performance to guide sales and expansion decisions
- **Self-service analysis:** slicers let users answer their own questions without new reports


---

## 📁 Repository Structure

```
├── images/          # Dashboard screenshots
├── sql/             # SQL scripts for staging, modeling, and KPI logic
├── python/          # Data cleansing & transformation scripts
├── ssis/            # SSIS package documentation
├── powerbi/         # Power BI report file (.pbix)
└── README.md
```
