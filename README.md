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
| Column Name         | Description                                                  |
|---------------------|--------------------------------------------------------------|
| `job_id`            | Year the salary was reported                                 |
| `job_title`         | Job title in the AI/ML field                                 |
| `salary_usd`        | Annual salary converted to USD                               |
| `salary_currency`   | Currency of the paid salary                                  |
| `experience_level`  | Junior, Mid, Senior, Executive                               |
| `employment_type`   | FT (Full-time), PT (Part-time), Contract, Freelance          |
| `company_location`  | Country of company                                           |
| `company_size`      | S (Small), M (Medium), L (Large)                             |
| `employee_residence`| Country of employee                                          |
| `remote_ratio`      | 0 = on-site, 50 = hybrid, 100 = fully remote                 |
| `required_skills `  | Skills required for the job                                  |
| `education_required`| Level of education                                           |
| `years_experience`  | Nummber of years experience                                  |
| `industry`          | Industry of the employer                                     |
| `posting_date`      | The date the job recruiter posted the JD                     |
| `application_deadline	`| deadline to submit the job application                    |
| `job_description_length	`  | length of the JD                 |
| `benefit_score`          | Benefit score of the company (1-10)                     |
| `company_name`          | Name of the company                                     |


---

## 🛠 Tools and Technologies Applied

- **Google Colab** – Interactive notebook platform
- **Python** – Core programming language
- **Pandas** – Data manipulation
- **Matplotlib & Seaborn** – Data visualization
- **NumPy** – Numerical operations
- **Collections** – Skill frequency analysis

---

## 📌 Key Insights Discovered

- **Role-based Pay**: AI leadership and research roles offer the highest salaries. Data and Engineer with high technical skill in robot and AI also get hefty pay.
- **Remote Work**: Fully remote jobs generally pay more, especially from U.S.-based firms. Especi
- **Regional Disparity**: North America leads in compensation compared to Europe and Asia.
- **Experience Premium**: Executives and senior professionals earn significantly more.
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
