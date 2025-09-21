# 📊 Business 360 Dashboard — AtliQ Hardware (Power BI)

## 🔗 Live Dashboard



[View Dashboard](https://app.powerbi.com/view?r=eyJrIjoiN2U0NDdiYmEtYzBkYS00NGFiLWE0YjQtZTUxODE4NjljNWJiIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9&pageName=056356e40818b8dab3c0)

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

Here are some Quick Snap of the Dashboard:


---


## 💬 Feedback & Contact

If you have suggestions or want collaboration/help, create an issue or contact: gangachakradhar2003@gmail.com.

---

