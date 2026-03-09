# Week 2 – Data Collection & Management

## 🎯 Learning Objectives

- Understand the data lifecycle and data governance principles
- Distinguish between structured and unstructured data
- Work with common file formats: CSV, JSON, XML, SQL
- Use Python and Power BI to summarise sales data

## 📚 Key Concepts

| Concept | Description |
|---------|-------------|
| Data Lifecycle | Collection → Storage → Processing → Analysis → Archiving |
| Structured Data | Tables, spreadsheets, relational databases |
| Unstructured Data | Text, images, video, social media |
| Data Governance | Policies and standards for data quality and access |

### File Formats

| Format | Use Case |
|--------|----------|
| CSV | Flat tabular data, widely compatible |
| JSON | APIs, nested/semi-structured data |
| XML | Legacy systems, config files |
| SQL | Relational databases |

---

## 📋 Group Project – Sales Summary

### Dataset
- **File:** `data/Week-2-Sales-Data.csv`

### Task Description

Using both **Python** and **Power BI**, summarise the sales data by:
- Product
- Region
- Revenue

### Python Requirements

- [ ] Load `Week-2-Sales-Data.csv` using `pandas`
- [ ] Group by **Product** → sum Revenue
- [ ] Group by **Region** → sum Revenue
- [ ] Print or export summary tables
- [ ] (Optional) Create basic charts using `matplotlib`

### Sample Python Starter Code

```python
import pandas as pd

# Load data
df = pd.read_csv('data/Week-2-Sales-Data.csv')

# Preview
print(df.head())
print(df.info())

# Summary by Product
product_summary = df.groupby('Product')['Revenue'].sum().reset_index()
print("\nSales by Product:")
print(product_summary)

# Summary by Region
region_summary = df.groupby('Region')['Revenue'].sum().reset_index()
print("\nSales by Region:")
print(region_summary)

# Export summaries
product_summary.to_csv('outputs/sales_by_product.csv', index=False)
region_summary.to_csv('outputs/sales_by_region.csv', index=False)
```

### Power BI Requirements

- [ ] Import `Week-2-Sales-Data.csv` into Power BI
- [ ] Create a bar chart: **Revenue by Product**
- [ ] Create a bar chart: **Revenue by Region**
- [ ] Add a card showing **Total Revenue**
- [ ] Save as `.pbix`

---

## 📁 Folder Structure

```
week-02/
├── README.md
├── data/
│   └── Week-2-Sales-Data.csv
├── outputs/
│   ├── Week2_Sales_Summary.pbix
│   ├── sales_by_product.csv
│   ├── sales_by_region.csv
│   └── week2_analysis.py
└── screenshots/
    └── powerbi_report.png
```

## ✅ Submission Checklist

- [ ] `week2_analysis.py` saved and runs without errors
- [ ] Power BI `.pbix` file saved in `outputs/`
- [ ] Both Python summaries exported as CSV
- [ ] Screenshot of Power BI report saved in `screenshots/`

---

## 🔗 Resources

- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Power BI – Getting Started](https://learn.microsoft.com/en-us/power-bi/fundamentals/desktop-getting-started)
