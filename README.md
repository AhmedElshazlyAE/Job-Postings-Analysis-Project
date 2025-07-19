# 📌 Introduction
This project focuses on analyzing a dataset of job postings to uncover key insights about hiring trends, required skills, company demands, and more. The goal is to use SQL to explore the data and answer relevant business questions that might help job seekers and HR professionals understand the job market better.

# 🖼️ Background
Through this project, I aimed to improve my SQL querying skills, data analysis mindset, and workflow using version control. The dataset was cleaned, explored, and analyzed using SQL queries, and the results were interpreted to draw meaningful conclusions.

Whether you're interested in data analysis or just curious about the current job market, this project gives a glimpse into how data-driven decision-making can help us better understand employment trends.

# 🛠️ Tools and Technologies Used
- PostgreSQL: Used to store, query, and analyze the job postings dataset.

- SQL For data cleaning, manipulation, and analysis.

- Visual Studio Code: My main editor for writing and testing SQL queries.

- Git: Version control system used to manage changes and collaborate effectively.

- GitHub: Hosting the project repository and sharing my work.

# The Analysis
Each Query In this project is aimed at providing Data Analysts with
information about the job market. Here is how I approached each 
question

### Top Paying data-analyst jobs
To show the highest paying roles I filtered each job by it's
average yearly salary then Ordered them descendingly to identify
which jobs pay the most

```sql
SELECT 
    job_id,
    job_title,
    job_location,
    job_schedule_type,
    job_posted_date::DATE,
    salary_year_avg
    
FROM job_postings_fact

WHERE
    salary_year_avg IS NOT NULL 
    AND job_title_short = 'Data Analyst'

ORDER BY salary_year_avg DESC --Ordering by yearly salary 

LIMIT 10
```

**Salary Range**
Top 10 Paying Data Analyst Roles Salaries Range From
285000$-650000$ showing a high salary potential in
the field

**Job Variety**
There's a high diversity in Job Titles, From Head Of Financial
Data Analytics to Director of Analytics Which reflects varied roles
and specialization in the field

### Skills required for these top-paying roles

TODO:
- What are the top paying data-analyst jobs (Done)
- What are the skills required for these top-paying roles (Done)
- What are the most in demand skills for a certain role (Done)
- What are the top skills based on salary for my role (Done)
- What are the most optimal skills to learn (High paying and High demand)
