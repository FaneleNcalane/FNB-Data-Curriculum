# Week 12 – Data Governance & Lineage in Power BI

## 🎯 Learning Objectives
- Understand data sensitivity labels and their importance
- Learn how to document a Power BI data model
- Introduce Row-Level Security (RLS) concepts
- Research real-world BI failures caused by poor data governance
- Align findings to the SFIA DATM skill

## 📚 Key Concepts

| Concept | Description |
|---------|-------------|
| Data Sensitivity Labels | Classify data as Public, Internal, Confidential, Highly Confidential |
| Data Lineage | Tracking where data comes from and how it flows |
| Row-Level Security (RLS) | Restricting data access based on user roles |
| Workspace Roles | Admin, Member, Contributor, Viewer in Power BI Service |
| DATM | SFIA skill: Data Management – governance, stewardship, quality |

---

## 📋 Group Task 2 – Research & Theory

### Task Description

Research a **real-world analytics or BI project that failed due to poor data governance**.

### Research Requirements

- [ ] Identify a real failed BI/analytics project (news article, case study, academic paper)
- [ ] Describe what went wrong (data quality, access issues, lineage, compliance)
- [ ] Explain how **Power BI governance features** could have prevented the failure:
  - **Row-Level Security (RLS)** – who sees what
  - **Lineage View** – tracking data flow
  - **Workspace Roles** – controlling access
- [ ] Map the failure and solution to the **SFIA DATM** skill framework
- [ ] Present findings to the group/trainer

### Presentation Structure

1. **Introduction** – What project failed? When? Who was affected?
2. **Root Cause** – What governance issue caused the failure?
3. **Power BI Solutions** – How RLS / Lineage / Roles would have helped
4. **SFIA DATM Alignment** – Which DATM responsibilities were violated?
5. **Lessons Learned** – Best practices for future projects

### RLS Example in Power BI

```dax
-- In Manage Roles → Create role "RegionManager"
-- Add table filter on Sales table:
[Region] = USERPRINCIPALNAME()

-- Or use a lookup table:
[Region] = LOOKUPVALUE(
    UserRoles[Region],
    UserRoles[Email], USERPRINCIPALNAME()
)
```

---

## 📁 Folder Structure

```
week-12/
├── README.md
├── data/                   ← No dataset required
├── outputs/
│   └── Group1_Week12_Governance_Presentation.pptx
└── screenshots/
    └── lineage_view_example.png
```

## ✅ Submission Checklist

- [ ] Real-world BI failure case identified and documented
- [ ] Power BI governance features (RLS, lineage, roles) explained
- [ ] SFIA DATM alignment included
- [ ] Presentation saved in `outputs/`
- [ ] Presented to group

---

## 🔗 Resources
- [SFIA DATM Skill](https://sfia-online.org/en/sfia-8/skills/data-management)
- [Row-Level Security in Power BI](https://learn.microsoft.com/en-us/power-bi/enterprise/service-admin-rls)
- [Data Lineage in Power BI Service](https://learn.microsoft.com/en-us/power-bi/collaborate-share/service-data-lineage)
- [Power BI Workspace Roles](https://learn.microsoft.com/en-us/power-bi/collaborate-share/service-roles-new-workspaces)
