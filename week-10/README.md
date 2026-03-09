# Week 10 – Segmentation & Grouping in Power BI

## 🎯 Learning Objectives
- Use binning and grouping features in Power BI
- Create customer segments using DAX calculated columns
- Build reports with segment-level insights and tooltips

## 📚 Key Concepts

| Concept | Description |
|---------|-------------|
| Binning | Grouping continuous values into ranges (e.g. Age 20–30) |
| Grouping | Combining categorical values into custom groups |
| Customer Segmentation | Classifying customers by behaviour or value |
| RFM Segmentation | Recency, Frequency, Monetary value model |

---

## 📋 Group Project – Customer Segmentation Report

### Dataset
- **File:** `data/Week-10-Customer-Segmentation.csv`
- **Columns expected:** `CustomerID`, `Age`, `Income`, `Spend`, `Region`

### Calculated Column (DAX)

```dax
Spend Segment =
IF(
    Customer_Segmentation[Spend] >= 8000, "High Spender",
    IF(
        Customer_Segmentation[Spend] >= 4000, "Medium Spender",
        "Low Spender"
    )
)
```

### Optional – Age Binning

```dax
Age Group =
IF(Customer_Segmentation[Age] < 30, "Under 30",
IF(Customer_Segmentation[Age] < 45, "30–44",
IF(Customer_Segmentation[Age] < 60, "45–59", "60+")))
```

### Report Requirements

- [ ] **Bar chart:** Total Spend by Segment
- [ ] **Bar/map chart:** Customers by Region
- [ ] **Slicer:** Spend Segment
- [ ] **Card:** Total Customers per Segment
- [ ] **Tooltips** on visuals showing additional context (e.g. avg income)

---

## 📁 Folder Structure

```
week-10/
├── README.md
├── data/
│   └── Week-10-Customer-Segmentation.csv
├── outputs/
│   └── Week10_Customer_Segmentation.pbix
└── screenshots/
    └── segmentation_report.png
```

## ✅ Submission Checklist

- [ ] `Spend Segment` calculated column created (Low/Medium/High)
- [ ] Report shows Spend by Segment, Customers by Region
- [ ] Segment slicer functional
- [ ] Tooltips configured on at least 1 visual
- [ ] `.pbix` saved in `outputs/`

---

## 🔗 Resources
- [Grouping and Binning in Power BI](https://learn.microsoft.com/en-us/power-bi/create-reports/desktop-grouping-and-binning)
- [DAX IF Function](https://learn.microsoft.com/en-us/dax/if-function-dax)
