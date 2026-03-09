# Week 13 – Business Intelligence & Reporting in Power BI

## 🎯 Learning Objectives
- Design professional, multi-page reports for management audiences
- Use buttons and navigation elements for interactive reports
- Create executive summaries and detail drill-down views

## 📚 Report Design Principles

| Principle | Application |
|-----------|-------------|
| Audience First | Executives want summaries; analysts want detail |
| Visual Hierarchy | Most important KPIs at the top |
| Consistent Layout | Same fonts, colors, margins across all pages |
| Navigation | Buttons for page-to-page flow |
| Whitespace | Don't overcrowd — let data breathe |

---

## 📋 Group Project – Business Performance Report

### Dataset
- **File:** `data/Week-13-Business-Performance.csv` *(or Power BI Financial Sample)*
- **Columns expected:** `Revenue`, `Expenses`, `Profit`, `Region`, `Department`, `CustomerSatisfaction`, `Date`

### Required DAX Measures

```dax
Total Revenue = SUM(Business_Performance[Revenue])
Total Expenses = SUM(Business_Performance[Expenses])
Total Profit = [Total Revenue] - [Total Expenses]
Profit Margin % = DIVIDE([Total Profit], [Total Revenue], 0)
Avg Customer Satisfaction = AVERAGE(Business_Performance[CustomerSatisfaction])
```

### Report Pages

**Page 1 – Executive Summary:**
- [ ] **Card:** Total Revenue
- [ ] **Card:** Total Expenses
- [ ] **Card:** Total Profit
- [ ] **Card:** Avg Customer Satisfaction (⭐ rating or gauge)
- [ ] **KPI visual** or trend chart
- [ ] "Next" button → navigates to Page 2

**Page 2 – Detail View:**
- [ ] **Bar chart:** Revenue by Region
- [ ] **Bar chart:** Revenue by Department
- [ ] **Table:** Top 10 rows detail view
- [ ] **Slicer:** Region and Department
- [ ] "Back" button → returns to Page 1

---

## 📁 Folder Structure

```
week-13/
├── README.md
├── data/
│   └── Week-13-Business-Performance.csv
├── outputs/
│   └── Week13_Business_Performance.pbix
└── screenshots/
    ├── executive_summary_page.png
    └── detail_view_page.png
```

## ✅ Submission Checklist

- [ ] Executive Summary page with Revenue, Expenses, Profit, Customer Sat
- [ ] Detail View page with region/department breakdown
- [ ] "Back" and "Next" navigation buttons working
- [ ] Slicers functional on Detail page
- [ ] `.pbix` saved in `outputs/`

---

## 🔗 Resources
- [Power BI Buttons for Navigation](https://learn.microsoft.com/en-us/power-bi/create-reports/desktop-buttons)
- [Financial Sample Dataset](https://learn.microsoft.com/en-us/power-bi/create-reports/sample-financial-download)
