# Week 3 – Data Cleaning & Preparation in Power BI

## 🎯 Learning Objectives

- Use Power Query Editor to clean and transform data
- Remove duplicates and handle missing (null) values
- Change data types and split columns
- Perform basic data quality checks
- Load cleaned data into the Power BI model

## 📚 Key Concepts

| Task | Power Query Step |
|------|-----------------|
| Remove duplicates | Home → Remove Rows → Remove Duplicates |
| Handle nulls | Replace Values / Remove Rows with Errors |
| Change data type | Click column header → Change Type |
| Split column | Transform → Split Column → By Delimiter |
| Data profiling | View → Column Quality / Column Distribution / Column Profile |

---

## 📋 Group Project – Employee Data Cleaning

### Dataset
- **File:** `data/Week-3-Employee-Data.csv`

### Task Description

Import and clean the employee dataset in Power BI, then build a simple report.

### Power Query Steps

- [ ] Import `Week-3-Employee-Data.csv` into Power BI
- [ ] Open **Power Query Editor**
- [ ] Remove duplicate rows
- [ ] Handle null values: fill down or remove rows with nulls
- [ ] Split the `FullName` column into `FirstName` and `LastName`
- [ ] Ensure correct data types for all columns (text, number, date)
- [ ] Close & Apply to load into the model

### Report Requirements

Build a simple 1-page report with:

- [ ] **Bar chart:** Number of Employees by Department
- [ ] **Bar chart:** Number of Employees by Location
- [ ] **Card:** Total Employee Count
- [ ] Title on the report page

---

## 📁 Folder Structure

```
week-03/
├── README.md
├── data/
│   └── Week-3-Employee-Data.csv
├── outputs/
│   └── Week3_Employee_Report.pbix
└── screenshots/
    ├── power_query_steps.png
    └── report_page.png
```

## ✅ Submission Checklist

- [ ] Data cleaned in Power Query (no duplicates, no nulls)
- [ ] `FullName` split into `FirstName` and `LastName`
- [ ] Report shows employees by department and location
- [ ] `.pbix` file saved in `outputs/`
- [ ] Screenshots of Power Query steps and report saved

---

## 🔗 Resources

- [Power Query – Remove Duplicates](https://learn.microsoft.com/en-us/power-query/remove-duplicates)
- [Power Query – Handle Null Values](https://learn.microsoft.com/en-us/power-query/replace-values)
- [Split Columns in Power Query](https://learn.microsoft.com/en-us/power-query/split-columns-delimiter)
