# Week 11 – Power BI for Data Engineering Concepts (Light ETL)

## 🎯 Learning Objectives
- Perform ETL (Extract, Transform, Load) operations using Power Query
- Append multiple query tables into one fact table
- Merge queries with dimension tables (lookup joins)
- Unpivot columns for better data modeling
- Build reusable, documented query steps

## 📚 ETL Operations in Power Query

| Operation | Description | Power Query Step |
|-----------|-------------|-----------------|
| Append | Stack tables vertically (same structure) | Home → Append Queries |
| Merge | Join tables horizontally (like SQL JOIN) | Home → Merge Queries |
| Unpivot | Convert columns to rows | Transform → Unpivot Columns |
| Group By | Aggregate rows | Transform → Group By |

---

## 📋 Group Project – Multi-Year Sales ETL

### Datasets
- **Files:** `data/Sales_2024.csv` and `data/Sales_2025.csv`
- **Dimension:** `data/Products.csv` (or similar dimension table)

### Power Query Steps

**Step 1 – Append:**
- [ ] Load `Sales_2024.csv` as Query 1
- [ ] Load `Sales_2025.csv` as Query 2
- [ ] Append Query 2 to Query 1 → creates a single `All_Sales` fact table

**Step 2 – Merge:**
- [ ] Merge `All_Sales` with `Products` on `ProductID`
- [ ] Expand the merged column to bring in `ProductName`, `Category`

**Step 3 – Clean & Transform:**
- [ ] Rename columns clearly
- [ ] Ensure consistent data types
- [ ] Remove any empty rows

### Report Requirements

- [ ] **Bar chart:** Sales by Year
- [ ] **Bar chart:** Sales by Product
- [ ] **Bar chart:** Sales by Category
- [ ] Screenshot of **Query Steps** panel in Power Query

---

## 📁 Folder Structure

```
week-11/
├── README.md
├── data/
│   ├── Sales_2024.csv
│   ├── Sales_2025.csv
│   └── Products.csv
├── outputs/
│   └── Week11_ETL_Sales_Report.pbix
└── screenshots/
    ├── query_steps.png
    └── report_page.png
```

## ✅ Submission Checklist

- [ ] Two sales files appended into one fact table
- [ ] Products dimension merged successfully
- [ ] Query steps clearly documented (screenshot)
- [ ] Report shows Sales by Year and Sales by Product
- [ ] `.pbix` saved in `outputs/`

---

## 🔗 Resources
- [Append Queries in Power Query](https://learn.microsoft.com/en-us/power-query/append-queries)
- [Merge Queries in Power Query](https://learn.microsoft.com/en-us/power-query/merge-queries-overview)
- [Unpivot Columns](https://learn.microsoft.com/en-us/power-query/unpivot-column)
