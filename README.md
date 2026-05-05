<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=1a1f5e&height=200&section=header&text=Data%20Professional%20Survey%20Breakdown&fontSize=36&fontColor=ffffff&fontAlignY=38&desc=Power%20BI%20Dashboard%20%7C%20630%20Respondents%20%7C%20Global%20Survey&descAlignY=58&descSize=16" width="100%"/>

<br/>

[![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-1a1f5e?style=for-the-badge&logo=microsoft&logoColor=white)](https://learn.microsoft.com/en-us/dax/)
[![Power Query](https://img.shields.io/badge/Power%20Query-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)](https://learn.microsoft.com/en-us/power-query/)
[![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)](/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-hanzalaraja-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/hanzalaraja)

</div>

---

## 📌 Project Overview

> A fully interactive Power BI dashboard built on a **real-world survey dataset** of **630 data professionals** from across the globe. This project covers the complete analytics workflow — from raw, messy data to a clean, insight-driven two-page dashboard — answering the key question:
>
> **_What does the data profession actually look like today?_**


---

## 🎯 Problem Statement

The raw survey data came with several critical issues that made direct analysis impossible:

| Problem | Description |
|--------|-------------|
| 📝 Salary as text | Salary was recorded as ranges like `60k–80k` instead of numeric values |
| 🌍 Inconsistent countries | Country names had multiple spellings and variations |
| 💼 Scattered job titles | Dozens of unique job title entries with no standardization |
| ❓ Open-ended responses | Free-text fields needed categorization before visualization |

**Goal:** Clean, transform, and model this data to build a dashboard that tells the real story of the data profession.

---

## 🔧 Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Power BI Desktop** | Dashboard design and visualization |
| **Power Query** | Data cleaning and transformation |
| **DAX** | Calculated measures and KPIs |
| **Excel** | Raw data source (.xlsx format) |

---

## 🧹 Data Cleaning Process (Power Query)

```
Raw Data (630 rows, 26 columns)
        │
        ▼
┌─────────────────────────────────────┐
│  Step 1: Salary Column              │
│  "60k-80k" → extracted midpoint     │
│  → converted to numeric (INT)        │
└──────────────┬──────────────────────┘
               │
               ▼
┌─────────────────────────────────────┐
│  Step 2: Job Title Standardization  │
│  Rare titles → grouped into "Other" │
│  Kept: Analyst, Scientist, Engineer │
│  Architect, Developer               │
└──────────────┬──────────────────────┘
               │
               ▼
┌─────────────────────────────────────┐
│  Step 3: Country Standardization    │
│  Low-frequency countries → "Other"  │
│  Kept top countries by volume       │
└──────────────┬──────────────────────┘
               │
               ▼
        Clean Dataset ✅
```

---

## 📊 DAX Measures Used

```dax
-- Average Salary
Avg Salary = AVERAGE('Survey'[Q3 - Current Yearly Salary (in USD)])

-- Average Age
Avg Age = AVERAGE('Survey'[Q10 - Current Age])

-- Work/Life Balance Score
Avg WorkLife = AVERAGE('Survey'[Q6 - Work/Life Balance])

-- Salary Satisfaction Score
Avg Salary Satisfaction = AVERAGE('Survey'[Q6 - Salary])

-- Coworker Satisfaction
Avg Coworkers = AVERAGE('Survey'[Q6 - Coworkers])

-- Management Satisfaction
Avg Management = AVERAGE('Survey'[Q6 - Management])

-- Upward Mobility Score
Avg Upward Mobility = AVERAGE('Survey'[Q6 - Upward Mobility])

-- Learning & Growth Score
Avg Learning = AVERAGE('Survey'[Q6 - Learning New Things])
```

---

## 📈 Dashboard Pages & Visuals

### Page 1: Survey Overview

| Visual | Type | Insight |
|--------|------|---------|
| Country of Survey Takers | Treemap | US leads, followed by India and UK |
| Average Salary by Job Title | Bar Chart | Data Scientists earn the most |
| Favorite Programming Language | Clustered Bar | Python dominates across all roles |
| Difficulty to Break into Data | Donut Chart | 42.7% say neither easy nor difficult |
| Satisfaction: Work/Life Balance | Gauge | 5.74 / 10 |
| Satisfaction: Salary | Gauge | 4.27 / 10 |
| Total Survey Takers | KPI Card | 630 |
| Average Age of Respondents | KPI Card | 29.87 |

### Page 2: Satisfaction & Demographics

| Visual | Type | Insight |
|--------|------|---------|
| Satisfaction: Coworkers | Gauge | 5.86 / 10 — highest satisfaction |
| Satisfaction: Learning & Growth | Gauge | 5.61 / 10 |
| Satisfaction: Management | Gauge | 5.33 / 10 |
| Satisfaction: Upward Mobility | Gauge | 4.76 / 10 |
| Most Important Factor in New Job | Bar Chart | Better Salary ranks #1 |
| Gender Distribution | Donut Chart | 74% Male, 26% Female |
| Highest Level of Education | Bar Chart | Bachelors degree most common |
| Industry of Data Professionals | Bar Chart | Tech and Finance lead |
| Age Distribution of Respondents | Donut Chart | 25–29 is the largest age group |

---

## 💡 Key Insights

```
┌─────────────────────────────────────────────────────────┐
│                   KEY FINDINGS                          │
├─────────────────────────────────────────────────────────┤
│  💰  Data Scientists earn the highest average salary    │
│  🐍  Python is the #1 language across ALL roles         │
│  📊  42.7% found breaking into data neither easy/hard   │
│  😐  Salary satisfaction is the LOWEST score (4.27/10)  │
│  🤝  Coworker satisfaction is the HIGHEST (5.86/10)     │
│  🎯  Better Salary is the top job search priority       │
│  🎓  Most professionals hold a Bachelor's degree        │
│  👥  74% of survey respondents are Male                 │
│  🏢  Tech and Finance are the top hiring industries     │
│  📅  Average professional age is 29.87 years            │
└─────────────────────────────────────────────────────────┘
```

---




## 🚀 How to Use

```bash
# Step 1: Clone the repository
git clone https://github.com/ThAnalyser/data-professional-survey-dashboard

# Step 2: Open the .pbix file in Power BI Desktop
# (Free download: https://powerbi.microsoft.com/desktop)

# Step 3: Explore the dashboard
# Use slicers to filter by country, job title, or gender
```

---

## 🤝 Connect With Me

<div align="center">

| Platform | Link |
|----------|------|
| 💼 LinkedIn | [linkedin.com/in/hanzalaraja](https://linkedin.com/in/hanzalaraja) |
| 🐙 GitHub | [github.com/ThAnalyser](https://github.com/ThAnalyser) |
| 📧 Email | Available on LinkedIn |

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=1a1f5e&height=100&section=footer" width="100%"/>

⭐ **If you found this project useful, please give it a star!** ⭐

*Built with 💙 by Raja Hanzala Muavia*

</div>
