# Week 7 – Power BI with DAX Basics

## 🎯 Learning Objectives
- Understand the difference between calculated columns and measures
- Write basic DAX functions: SUM, COUNTROWS, DIVIDE, IF
- Build KPI dashboards with target vs actual comparisons

## 📚 DAX Reference

### Calculated Column vs Measure

| | Calculated Column | Measure |
|--|-------------------|---------|
| Computed | Row-by-row | Aggregated (context-dependent) |
| Stored | In the table | Dynamically at query time |
| Use for | Categorising, flags | KPIs, totals, ratios |

### Key DAX Functions

```dax
-- Totals
Total Sales = SUM(Orders[Revenue])
Total Quantity = SUM(Orders[Quantity])

-- Counting
Total Orders = COUNTROWS(Orders)

-- Safe division (avoids divide-by-zero)
Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)

-- Conditional
High Value Order = IF(Orders[Revenue] > 1000, "High", "Standard")
```

---

## 📋 Group Project – Orders KPI Dashboard

### Dataset
- **File:** `data/Week-7-PowerBI-Orders.csv` *(or Power BI Retail Analysis Sample)*

### Measures to Create

- [ ] `Total Sales = SUM(Orders[Revenue])`
- [ ] `Total Quantity = SUM(Orders[Quantity])`
- [ ] `Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)` *(if Profit column exists)*
- [ ] `Sales Target` – hardcoded or from a target table

### Report Requirements

- [ ] **KPI visual:** Actual Sales vs Sales Target
- [ ] **Card:** Total Sales, Total Quantity, Profit Margin %
- [ ] **Slicer:** Region
- [ ] **Slicer:** Product Category
- [ ] **Bar chart:** Sales by Category

---

## 📁 Folder Structure

```
week-07/
├── README.md
├── data/
│   └── Week-7-PowerBI-Orders.csv
├── outputs/
│   └── Week7_DAX_KPI_Dashboard.pbix
└── screenshots/
    └── kpi_dashboard.png
```

## ✅ Submission Checklist

- [ ] At least 3 DAX measures created
- [ ] KPI visual showing target vs actual
- [ ] Region and Category slicers added
- [ ] `.pbix` saved in `outputs/`
- [ ] Screenshot saved

---

## 🔗 Resources
- [DAX Overview – Microsoft](https://learn.microsoft.com/en-us/dax/dax-overview)
- [KPI Visual in Power BI](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-kpi)
