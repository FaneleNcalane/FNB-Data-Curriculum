# Week 15 – End-to-End Analytics Project in Power BI

## 🎯 Learning Objectives
- Execute a complete analytics pipeline: Get Data → Transform → Model → Visualise → Publish
- Independently apply all skills from Weeks 1–14
- Build a professional, multi-page Power BI report from scratch
- Document the full analytical process

## 📚 End-to-End Pipeline

```
Raw Data (CSV)
    │
    ▼
[Power Query – Transform & Clean]
    │  • Remove nulls/duplicates
    │  • Fix data types
    │  • Merge/Append if needed
    ▼
[Model View – Relationships]
    │  • Define table relationships
    │  • Star schema if applicable
    ▼
[DAX – Measures & Columns]
    │  • KPIs, ratios, segments
    ▼
[Report Canvas – Visualise]
    │  • Overview page
    │  • Detail page
    │  • Slicers, cards, charts
    ▼
[Export / Publish]
    • PDF export
    • .pbix saved
```

---

## 📋 Group Project – Analytics Pipeline Report

### Dataset
- **File:** `data/Week-15-Analytics-Pipeline.csv`

### Power Query (Transform) Requirements

- [ ] Remove duplicates and null rows
- [ ] Correct data types for all columns
- [ ] Create at least 1 additional transform step (e.g. split column, add custom column)
- [ ] Document all steps (they appear in Applied Steps panel)

### DAX Measures (at least 3)

```dax
-- Example measures (adapt to your dataset columns)
Total Revenue = SUM(Analytics_Pipeline[Revenue])
Total Customers = DISTINCTCOUNT(Analytics_Pipeline[CustomerID])
Avg Revenue per Customer = DIVIDE([Total Revenue], [Total Customers], 0)
```

### Report Pages

**Page 1 – Overview:**
- [ ] At least 2 KPI cards
- [ ] 1 trend chart (line or bar)
- [ ] 1 slicer
- [ ] Report title

**Page 2 – Detail:**
- [ ] Deeper breakdown (by region, category, time period)
- [ ] Table or matrix visual
- [ ] Additional slicer
- [ ] Navigation button back to Overview

---

## 📁 Folder Structure

```
week-15/
├── README.md
├── data/
│   └── Week-15-Analytics-Pipeline.csv
├── outputs/
│   ├── Week15_End_to_End_Report.pbix
│   └── Week15_End_to_End_Report.pdf
└── screenshots/
    ├── power_query_steps.png
    ├── model_view.png
    ├── overview_page.png
    └── detail_page.png
```

## ✅ Submission Checklist

- [ ] Data cleaned in Power Query (steps visible)
- [ ] At least 3 DAX measures created
- [ ] 2 report pages (Overview + Detail)
- [ ] At least 1 slicer and 1 card on each page
- [ ] Report exported to PDF
- [ ] `.pbix` saved in `outputs/`
- [ ] All screenshots saved

---

## 🔗 Resources
- [Power BI End-to-End Tutorial](https://learn.microsoft.com/en-us/power-bi/create-reports/desktop-excel-stunning-report)
- [Star Schema in Power BI](https://learn.microsoft.com/en-us/power-bi/guidance/star-schema)
