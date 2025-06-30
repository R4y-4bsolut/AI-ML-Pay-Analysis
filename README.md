# 💼 AI/ML Salary Market Analysis

This project investigates salary trends across roles, industries, regions from 2024 to 3/2025 in Artificial Intelligence (AI) and Machine Learning (ML) to gain insights into the global job market and provide actionable recommendations for job seekers, employers, and analysts.

---

## 🎯 Goals of the Project

- Analyze salary data for AI/ML-related roles across different regions, experience levels, company sizes, and industries.
- Identify trends, disparities, and patterns in global compensation.
- Generate data-driven hypotheses and practical recommendations.

---

## 🗂 Data Sources Used

- **Primary Dataset**: [AI/ML Salary Dataset](https://www.kaggle.com/datasets/jessemostipak/artificial-intelligence-jobs)  
  Sourced from Kaggle, the dataset aggregates AI/ML-related job data including salaries, job titles, and company information from global listings.

---

## 🧾 Data Overview

- **Format**: Single CSV file loaded into a Pandas DataFrame.
- **Structure**: Each row represents one AI/ML job record.

### Key Columns:
| Column Name         | Description                                                  | Datatype |
|---------------------|--------------------------------------------------------------|----------|
| `job_id`            | Year the salary was reported                                 |object    |
| `job_title`         | Job title in the AI/ML field                                 |int64     |
| `salary_usd`        | Annual salary converted to USD                               |object    |
| `salary_currency`   | Currency of the paid salary                                  |object    |
| `experience_level`  | Junior, Mid, Senior, Executive                               |object    |
| `employment_type`   | FT (Full-time), PT (Part-time), Contract, Freelance          |object    |
| `company_location`  | Country of company                                           |object    |
| `company_size`      | S (Small), M (Medium), L (Large)                             |object    |
| `employee_residence`| Country of employee                                          |object    |
| `remote_ratio`      | 0 = on-site, 50 = hybrid, 100 = fully remote                 |int64     |
| `required_skills `  | Skills required for the job                                  |object    |
| `education_required`| Level of education                                           |object    |
| `years_experience`  | Nummber of years experience                                  |int64     |
| `industry`          | Industry of the employer                                     |object    |
| `posting_date`      | The date the job recruiter posted the JD                     |object    |
| `application_deadline	`| deadline to submit the job application                    |object    |
| `job_description_length	`  | length of the JD                     | int64 |
| `benefit_score`          | Benefit score of the company (1-10)                     | float64  |
| `company_name`          | Name of the company                                     |object    |


---

## 🛠 Tools and Technologies Applied

- **Google Colab** – Interactive notebook platform
- **Python** – Core programming language
- **Power BI** – Data visualization

---
## ⚙️ Data Cleaning Process
### 1. Drop Unwanted Columns:
- The goal of this project is to analyse AI/ML trends and forecast market demand. Thus, columns that directly affect salary, job roles, demand indicators and context that are vital for the analysis will be kept, while unecessary columns will be excluded.

**Drop columns:**
1. _salary_currency_: salary_usd already standardises the pay currency.

2. _application_deadline_: not affecting the salary trends nor contributing to pay analysis.

3. _company_name_: this project has no intent to analyse company-specific data.

4. _job_description_length_: not significantly align with the project's scope.

5. _benefits_score_: Though could be useful for comparing benefit and salary offer, it still not significantly align with the project's scope.
### Revised Columns:
| Column Name         | Description                                                  | Datatype |
|---------------------|--------------------------------------------------------------|----------|
| `job_id`            | Year the salary was reported                                 |object    |
| `job_title`         | Job title in the AI/ML field                                 |int64     |
| `salary_usd`        | Annual salary converted to USD                               |object    |
| `experience_level`  | Junior, Mid, Senior, Executive                               |object    |
| `employment_type`   | FT (Full-time), PT (Part-time), Contract, Freelance          |object    |
| `company_location`  | Country of company                                           |object    |
| `company_size`      | S (Small), M (Medium), L (Large)                             |object    |
| `employee_residence`| Country of employee                                          |object    |
| `remote_ratio`      | 0 = on-site, 50 = hybrid, 100 = fully remote                 |int64     |
| `required_skills `  | Skills required for the job                                  |object    |
| `education_required`| Level of education                                           |object    |
| `years_experience`  | Nummber of years experience                                  |int64     |
| `industry`          | Industry of the employer                                     |object    |
| `posting_date`      | The date the job recruiter posted the JD                     |object    |

### 2. Check Data Consistency:
- The dataset contains 0 null values ✅
- The data set has no duplicates ✅

### 3. Remove Outliers
- The salary_usd is the only column that may contain outliers affecting overall analysis. So they were removed using IQR.
### 4. Change Datatype:
- Convert all columns into the right datatype.
---
## EDA PROCESS
- To conduct a descriptive analysis, the dataset was analysed and visualised by these following steps:
  1. UNIVARIATE ANALYSIS: analysing each column (distribution, frequency) to examinate overall data.
  2. BIVARIATE ANALYSIS: analysing 2 columns and seek for noteworthy patterns.
  3. MULTIVARIATE ANALYSIS: Lastly, from findings at previous analysis, grouping multiple columns to analyse detail scenarios.

---

## 📌 Key Insights Discovered

- **Role-based Pay**: AI leadership and research roles offer the highest salaries. Data and Engineer with high technical skill in robot and AI also get hefty pay.
- **Remote Work**: Fully remote jobs generally pay more, especially from U.S.-based firms. Especially, contract workers even get paid higher.
- **Regional Disparity**: North America leads in compensation compared to Europe and Asia. Asia is the region with the lowest average pay, with Singapore the only country in DF that offers high pay. In Europe, Switzerland, Denmark, Norway, and the UK holds the record for top 5 of the highest pay globally.
- **Experience Premium**: Executives and senior professionals earn significantly more. 
Entry to Mid: 39.32% 
Mid to Senior: 38.92%
Senior to Executive: 40.24%
- **Company Size Influence**: Large companies pay more on average, though some mid-sized firms offer competitive packages.


---

## ✅ Recommendations Based on Analysis

### For Job Seekers:
- Focus on high-demand niches (e.g., NLP, Deep Learning).
- Target remote roles with U.S. or global firms for better compensation.
- Prioritize experience and skills growth to climb pay brackets.

### For Employers:
- For employees residence at the Europe, prioritse fining positions in domestic companies instead of foreign firms.
- Focus on learning and improving AI/ML technical skills like Scala, Deep Learning and using Git more.
- For new employees, finding temporary contracts with US companies may get better pay than industry average.

---

## 🔍 Hypotheses Based on Insights

1. Remote work levels the playing field, allowing companies to hire global talent while offering above-local-market pay.
2. Research-heavy and strategic roles yield higher business impact, hence higher compensation.
3. Mid-sized firms might overpay in specialized roles to attract rare talent and stay competitive.
---
## 📎 How to Run

> Open this project in [Google Colab](https://colab.research.google.com/drive/16V8KD-wk88ocnGOtJKxGHNWsiNN9K4w_?usp=sharing), run all cells sequentially, and explore the generated visual insights.

---

## 📬 Contributions

Feel free to fork this repository and add:
- Time-series trend analysis
- Skills vs salary breakdown
- Real-time data pipeline integration (e.g., via APIs)
