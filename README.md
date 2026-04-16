# 📊 Data Professional Survey — Power BI Dashboard



## 📌 Overview

This project visualizes and analyzes survey responses collected from **630 data professionals** worldwide. The dataset captures insights into career roles, compensation, work-life satisfaction, programming language preferences, and the challenges of breaking into the data field.





---

## 📋 Dataset Overview

- **Source:** Online survey (collected June 2022)
- **Responses:** 630 data professionals
- **Sheet:** `Data Professional Survey`

### Key Columns

| Column | Description |
|--------|-------------|
| Q1 — Current Role | Job title (Data Analyst, Data Engineer, Data Scientist, etc.) |
| Q2 — Career Switch | Whether respondent switched careers into data |
| Q3 — Yearly Salary (USD) | Salary range (e.g., 0–40k, 41–65k, up to 225k+) |
| Q4 — Industry | Sector of employment (Tech, Finance, Healthcare, etc.) |
| Q5 — Favorite Language | Preferred programming language (Python, R, SQL, etc.) |
| Q6 — Happiness (6 dimensions) | Satisfaction ratings for Salary, Work/Life Balance, Coworkers, Management, Upward Mobility, Learning |
| Q7 — Difficulty Breaking In | Perceived difficulty entering the data field |
| Q8 — Job Priority | Most important factor when looking for a new job |
| Q9–Q13 | Demographics: Gender, Age, Country, Education, Ethnicity |

---

## 📊 Dashboard Highlights

The Power BI report covers:

- **Salary distribution** by job title and country
- **Career switcher analysis** — who transitioned into data and from where
- **Top programming languages** by role and region
- **Happiness scores** across 6 workplace dimensions
- **Difficulty of entry** into the data field
- **Job priority preferences** — remote work, better salary, good culture, etc.
- **Demographics breakdown** — age, gender, education level, and geography

---

## 🧹 Data Cleaning & Transformation

All cleaning and transformation was performed inside **Power Query** before loading data into the data model.

### Data Cleaning
- Removed irrelevant metadata columns (Browser, OS, City, Referrer, Time Spent) that added no analytical value
- Handled blank and null values across salary, happiness, and demographic fields
- Standardized free-text entries in Q1 (job titles), Q4 (industries), and Q5 (programming languages) — e.g., consolidating `"Business Analyst"`, `"BI Developer"`, and `"Analytics Consultant"` under cleaner categories
- Removed duplicate or near-duplicate entries based on Unique ID

### Data Transformation
- **Salary column (Q3):** Split the salary range string (e.g., `"41k-65k"`) into two numeric columns (Min Salary, Max Salary), then calculated an **Average Salary** column for use in visuals
- **Programming language (Q5):** Extracted and standardized `Other:` prefix entries (e.g., `"Other:SQL"`, `"Other:DAX"`) into a clean language label
- **Age (Q10):** Kept as a numeric field; outlier values (e.g., age 92) were flagged
- **Country (Q11):** Standardized `"Other (Please Specify):"` entries by extracting the actual country name for geographic visuals
- **Happiness scores (Q6):** Confirmed all values fall within a 0–10 scale; empty cells treated as null (excluded from averages)
- Created calculated columns and measures using **DAX** for KPIs like average salary by role, average happiness by dimension, and count of career switchers

---

## 🛠️ Tools Used

- **Microsoft Power BI Desktop** — report building, DAX calculations, and interactive visuals
- **Power Query (M language)** — data cleaning, transformation, and column creation
- **Microsoft Excel** — raw data source

---



## 📌 Key Insights (from the data)

### 💰 Salary
- **Data Scientists and Senior roles** (Analytics Manager, Director of Analytics) report the highest salaries, frequently in the **$125k–$225k+** range
- The majority of respondents, especially from **India, Nigeria, and Latin America**, fall in the **$0–40k** bracket, reflecting significant geographic pay disparity
- **Finance and Tech** industries offer higher compensation compared to Healthcare and Education

### 💻 Programming Languages
- **Python** is the dominant language across nearly all roles — Data Analysts, Data Engineers, and Data Scientists alike
- **R** is the second most preferred, particularly among analysts in Healthcare and Education
- **SQL** appears frequently as a write-in under "Other," suggesting it's widely used but underrepresented in the original options

### 😊 Job Satisfaction
- **Work/Life Balance** and **Coworkers** consistently score higher than **Salary** and **Upward Mobility**
- **Salary satisfaction** has some of the lowest average ratings across all roles — even higher earners rate it modestly
- Respondents in **senior or managerial roles** tend to report higher happiness across all six dimensions

### 🔄 Career Transitions
- A large share of respondents **switched careers** into data — particularly Data Analysts and Data Scientists
- Career switchers are spread across all age groups, with a notable cluster in the **late 20s to mid-30s**

### 🚪 Breaking Into Data
- The most common response to difficulty was **"Difficult"** or **"Very Difficult"**, especially among respondents from **Africa and South Asia**
- Those who self-identified as **Student/Looking/None** rated entry difficulty the highest

### 🌍 Demographics
- Respondents span **60+ countries**, with the highest representation from the **United States, India, United Kingdom, and Canada**
- The survey skews **male**, though female representation is notable in Healthcare, Education, and Finance sectors
- **Bachelor's and Master's degrees** are the most common education levels among working professionals

---

## 👤 Author

**Raja Hanzala Muavia**
📧 hanzala.analyst@gmail.com
🔗 [LinkedIn](https://linkedin.com/in/hanzalaraja) | [GitHub](https://github.com/ThAnalyser)

---

## 📄 License

This project is for educational and portfolio purposes.
