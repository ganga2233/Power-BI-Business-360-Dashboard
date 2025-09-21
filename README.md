# 📊 Business 360 Dashboard — AtliQ Hardware (Power BI)

## 🔗 Live Dashboard

> **Interactive report:** Replace the placeholder link below with your Power BI published/report link (if you published it to Power BI Service).

`https://app.powerbi.com/links/REPLACE_WITH_YOUR_LINK`

---

## 📌 Project Summary

A polished, end-to-end Power BI solution for **AtliQ Hardware** that integrates Finance, Sales, HR, and Supply Chain data into a single interactive dashboard. The report provides a 360° view of business performance to enable data-driven decisions at operational and executive levels.

---

## 🎯 Objectives

* Visualize **financial performance** (Revenue, Gross Margin, Net Profit, YTD, YTG)
* Surface **sales insights** (top/bottom customers, product trends, regional performance)
* Track **Marketing inshights** (Product Performances, Key metrics , Region Wise Performance, Performance metrics )
* Monitor **supply chain** KPIs (forecast accuracy, lead time, fulfilment reliability)
* Provide an **executive summary** page for leadership with primary KPIs and quick actions

---

## 🔍 Key Features

* **End-to-end ETL**: Power Query transformations to clean and standardize data
* **Star schema modeling**: Fact and dimension tables with optimized relationships
* **Advanced DAX measures**: Time intelligence, rolling totals, ratios, contribution analysis
* **Interactive UX**: Drill-through, bookmarks, slicers, tooltips, and cross-filtering
* **Performance tuning**: DAX Studio checks, optimized measures, and query reduction techniques

---

## 🛠 Tech Stack

* **Power BI Desktop** — report development
* **Power BI Service** — report sharing & publishing (optional)
* **DAX** — measures and business logic
* **Power Query (M)** — ETL transformations
* **MySQL / CSV / Excel** — data sources (replace with your actual sources)
* **DAX Studio** — performance analysis and optimization

---

## 📈 Example KPIs & Measures (copy-ready)

> Paste these sample DAX measures into your report and adapt table/column names as needed.

**Total Revenue**

```DAX
Total Revenue = SUM('Sales'[Revenue])
```

**Total Cost**

```DAX
Total Cost = SUM('Sales'[Cost])
```

**Gross Profit**

```DAX
Gross Profit = [Total Revenue] - [Total Cost]
```

**Gross Margin %**

```DAX
Gross Margin % = DIVIDE([Gross Profit], [Total Revenue], 0)
```

**YTD Revenue**

```DAX
YTD Revenue =
CALCULATE(
    [Total Revenue],
    DATESYTD('Date'[Date])
)
```

**Rolling 12 Months Revenue**

```DAX
Rolling 12M Revenue =
CALCULATE(
    [Total Revenue],
    DATESINPERIOD('Date'[Date], LASTDATE('Date'[Date]), -12, MONTH)
)
```

**Top 5 Customers by Revenue** (table visual - use Top N filter on Customer)

```DAX
Customer Revenue = SUM('Sales'[Revenue])
```

---

## 📸 Screenshots

Add exported PNGs of your main report pages to `/screenshots` and reference them here.

Example:

```
/screenshots/executive_overview.png
/screenshots/sales_dashboard.png
/screenshots/finance_dashboard.png
```

---

## 📂 Repository Structure (recommended)

```
business-360-powerbi/
├── README.md
├── business-360.pbix
├── /data                 # (optional) sample or anonymized datasets
├── /screenshots
├── /docs                 # project notes, ETL steps, DAX catalog
└── LICENSE
```

---

## 🚀 How to use

1. Clone the repo
2. Open `business-360.pbix` in Power BI Desktop
3. If data connections are to external sources, update connection strings or replace with sample CSVs in `/data`
4. Refresh data and explore report pages

---

## ✅ Documentation & Notes

* Add a `docs/DAX-measures.md` file containing all custom DAX measures with short descriptions and use-cases.
* Add `docs/data_dictionary.md` explaining table/column meanings and any data transformations performed in Power Query.

---

## 💬 Feedback & Contact

If you have suggestions or want collaboration/help, create an issue or contact: `your.email@example.com`.

---

## 📜 License

Add a license file (e.g., `LICENSE` with MIT) if you want to make this repo open-source.

---

*Made with ❤️ — ready for showcasing in portfolios, LinkedIn, and recruiter applications.*
