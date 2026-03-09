# Week 4 – Working with Databases in Power BI

## 🎯 Learning Objectives
- Connect Power BI to multiple related tables
- Create table relationships in Model view
- Use GROUP BY logic through visuals and DAX (not SQL)
- Build reports with slicers for filtering

## 📚 Key Concepts

| Concept | Description |
|---------|-------------|
| Relationships | Linking tables via shared keys (e.g. OrderID, ProductID) |
| Cardinality | One-to-many, many-to-one relationships |
| Model View | Visual interface to manage table relationships in Power BI |
| DAX Aggregations | SUM(), COUNT(), AVERAGE() replacing SQL GROUP BY |

---

## 📋 Group Project – Multi-Table Sales Report

### Dataset
- **Files:** `data/Customers.csv`, `data/Orders.csv`, `data/Products.csv`
- *(Or use AdventureWorks sample from Power BI)*

### Power BI Steps

- [ ] Load all 3 tables into Power BI
- [ ] Switch to **Model View** and create relationships:
  - `Orders[CustomerID]` → `Customers[CustomerID]`
  - `Orders[ProductID]` → `Products[ProductID]`
- [ ] Verify relationship cardinality (one-to-many)

### Report Requirements

- [ ] **Bar chart:** Sales by Region
- [ ] **Bar chart:** Top Products by Revenue
- [ ] **Table visual:** Orders by Customer (Name, Total Orders, Total Spend)
- [ ] **Slicer:** Year or Region
- [ ] At least 1 DAX measure (e.g. `Total Sales = SUM(Orders[Revenue])`)

### Sample DAX Measures

```dax
Total Sales = SUM(Orders[Revenue])

Total Orders = COUNTROWS(Orders)

Average Order Value = DIVIDE([Total Sales], [Total Orders])
```

---

## 📁 Folder Structure

```
week-04/
├── README.md
├── data/
│   ├── Customers.csv
│   ├── Orders.csv
│   └── Products.csv
├── outputs/
│   └── Week4_Database_Report.pbix
└── screenshots/
    ├── model_view_relationships.png
    └── report_page.png
```

## ✅ Submission Checklist

- [ ] At least 3 tables loaded
- [ ] Relationships created in Model View
- [ ] Report has Sales by Region, Top Products, Orders by Customer
- [ ] At least 1 slicer added
- [ ] `.pbix` saved in `outputs/`
- [ ] Screenshot of Model View relationships saved

---

## 🔗 Resources
- [Create Relationships in Power BI](https://learn.microsoft.com/en-us/power-bi/transform-model/desktop-create-and-manage-relationships)
- [AdventureWorks Sample](https://learn.microsoft.com/en-us/power-bi/create-reports/sample-datasets)
