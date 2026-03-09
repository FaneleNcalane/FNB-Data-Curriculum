# Week 5 – Exploratory Data Analysis (EDA) in Power BI

## 🎯 Learning Objectives
- Use column quality, distribution, and profiling tools in Power Query
- Calculate descriptive statistics using Quick Measures
- Create calculated columns with conditional logic
- Use slicers to explore and filter data interactively

## 📚 Key Concepts

| Concept | Description |
|---------|-------------|
| Column Quality | % valid, error, empty values per column |
| Column Distribution | Value frequency histogram |
| Column Profile | Min, max, average, distinct count |
| Calculated Column | New column computed row-by-row in DAX |

---

## 📋 Group Project – Student Scores EDA

### Dataset
- **File:** `data/Week-5-Student-Scores.csv`

### Power Query Steps
- [ ] Import dataset → open Power Query Editor
- [ ] Enable **Column Quality**, **Column Distribution**, **Column Profile** (View tab)
- [ ] Document findings: any nulls? outliers? unexpected values?

### Calculated Column (DAX)

```dax
Result = IF(Student_Scores[Marks] >= 50, "Pass", "Fail")
```

### Report Requirements

- [ ] **Bar chart:** Average Score by Subject
- [ ] **Table or bar chart:** Top 5 Students by Marks
- [ ] **Donut/bar chart:** Pass vs Fail count
- [ ] **Slicer:** Class or Grade
- [ ] **Card:** Total Students

---

## 📁 Folder Structure

```
week-05/
├── README.md
├── data/
│   └── Week-5-Student-Scores.csv
├── outputs/
│   └── Week5_EDA_Student_Scores.pbix
└── screenshots/
    ├── column_profile.png
    └── report_page.png
```

## ✅ Submission Checklist

- [ ] Column profiling done in Power Query
- [ ] `Result` calculated column created (Pass/Fail)
- [ ] Report shows avg score by subject, top 5 students, pass/fail
- [ ] Class/Grade slicer added
- [ ] `.pbix` saved in `outputs/`

---

## 🔗 Resources
- [Column Profiling in Power Query](https://learn.microsoft.com/en-us/power-query/data-profiling-tools)
- [DAX IF Function](https://learn.microsoft.com/en-us/dax/if-function-dax)
