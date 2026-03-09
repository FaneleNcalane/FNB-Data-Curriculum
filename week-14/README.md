# Week 14 – Advanced Power BI Features

## 🎯 Learning Objectives
- Create and use parameterized queries in Power Query
- Build What-if parameter sliders with DAX
- Use decomposition tree and Key Influencers visuals
- Analyse how business levers (e.g. discount %) affect revenue

## 📚 Key Features

| Feature | Description |
|---------|-------------|
| What-if Parameter | Creates a slicer that feeds into a DAX measure |
| Parameterized Query | Dynamic filter input in Power Query |
| Decomposition Tree | Visual drill-down to find root causes |
| Key Influencers | AI visual that identifies factors driving a metric |

---

## 📋 Group Project – Customer Behavior Analysis

### Dataset
- **File:** `data/Week-14-Customer-Behavior.csv`
- **Columns expected:** `CustomerID`, `Revenue`, `Discount`, `Category`, `Region`, `Churn`

### What-if Parameter Setup

1. Go to **Modeling → New Parameter**
2. Name: `Discount %`
3. Data type: Decimal Number
4. Min: 0, Max: 0.5, Increment: 0.05
5. Power BI creates: a slicer + a `Discount % Value` measure

### DAX Measures Using What-if

```dax
Adjusted Revenue =
[Total Revenue] * (1 - 'Discount %'[Discount % Value])

Revenue Impact =
[Total Revenue] - [Adjusted Revenue]
```

### Report Requirements

- [ ] **What-if parameter slicer:** Discount %
- [ ] **Card:** Original Revenue
- [ ] **Card:** Adjusted Revenue (after discount)
- [ ] **Card:** Revenue Impact (loss from discount)
- [ ] **Line/bar chart:** Adjusted Revenue by Category
- [ ] **Key Influencers visual** (if Churn column exists — analyse what drives churn)
- [ ] **Decomposition Tree** (optional — decompose Revenue by Region → Category → Product)

---

## 📁 Folder Structure

```
week-14/
├── README.md
├── data/
│   └── Week-14-Customer-Behavior.csv
├── outputs/
│   └── Week14_Advanced_Features.pbix
└── screenshots/
    ├── whatif_parameter.png
    └── key_influencers.png
```

## ✅ Submission Checklist

- [ ] What-if Discount % parameter created
- [ ] Adjusted Revenue measure created and working
- [ ] Revenue impact shown dynamically on report
- [ ] Key Influencers or Decomposition Tree visual added
- [ ] `.pbix` saved in `outputs/`

---

## 🔗 Resources
- [What-if Parameters in Power BI](https://learn.microsoft.com/en-us/power-bi/transform-model/desktop-what-if)
- [Key Influencers Visual](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-influencers)
- [Decomposition Tree](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-decomposition-tree)
