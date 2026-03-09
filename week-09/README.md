# Week 9 – Analytical Functions & What-if in Power BI

## 🎯 Learning Objectives
- Use DAX time intelligence functions (SAMEPERIODLASTYEAR)
- Calculate percentage change between periods
- Simulate A/B testing analysis using calculated measures
- Compare control vs treatment groups in a report

## 📚 Key DAX Functions

```dax
-- Year-over-year comparison
Sales Last Year = CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Date'[Date]))

-- Percentage change
YoY Growth % = DIVIDE([Total Sales] - [Sales Last Year], [Sales Last Year], 0)

-- A/B Testing measures
Control Conversions = CALCULATE(SUM(ABTest[Conversions]), ABTest[Group] = "Control")
Treatment Conversions = CALCULATE(SUM(ABTest[Conversions]), ABTest[Group] = "Treatment")

Control Rate = DIVIDE([Control Conversions], CALCULATE(SUM(ABTest[Visitors]), ABTest[Group] = "Control"), 0)
Treatment Rate = DIVIDE([Treatment Conversions], CALCULATE(SUM(ABTest[Visitors]), ABTest[Group] = "Treatment"), 0)

Conversion Rate Difference = [Treatment Rate] - [Control Rate]
```

---

## 📋 Group Project – A/B Testing Analysis

### Dataset
- **File:** `data/Week-9-ABTesting.csv`
- **Columns expected:** `Group` (Control/Treatment), `Conversions`, `Visitors`, `Date`

### Measures to Create

- [ ] `Total Conversions (Control)`
- [ ] `Total Conversions (Treatment)`
- [ ] `Conversion Rate (Control) = Conversions / Visitors`
- [ ] `Conversion Rate (Treatment) = Conversions / Visitors`
- [ ] `Difference in Conversion Rate`

### Report Requirements

- [ ] **Bar chart:** Conversion Rate – Control vs Treatment
- [ ] **Cards:** Conversion rates for each group
- [ ] **Card:** Rate Difference (formatted as %)
- [ ] **Text box:** Analysis conclusion — *"Which variant performed better and why?"*
- [ ] Slicer by Date (if available)

---

## 📁 Folder Structure

```
week-09/
├── README.md
├── data/
│   └── Week-9-ABTesting.csv
├── outputs/
│   └── Week9_ABTest_Analysis.pbix
└── screenshots/
    └── ab_test_report.png
```

## ✅ Submission Checklist

- [ ] All 4 A/B testing measures created
- [ ] Report visually compares Control vs Treatment
- [ ] Text box with conclusion included
- [ ] `.pbix` saved in `outputs/`

---

## 🔗 Resources
- [DAX CALCULATE Function](https://learn.microsoft.com/en-us/dax/calculate-function-dax)
- [SAMEPERIODLASTYEAR](https://learn.microsoft.com/en-us/dax/sameperiodlastyear-function-dax)
- [A/B Testing Basics](https://www.optimizely.com/optimization-glossary/ab-testing/)
