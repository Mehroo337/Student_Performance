# 🧮 Student Performance Analysis — SQL Project

### 🧠 Overview
This project explores student performance data using **PostgreSQL** to analyze academic outcomes and uncover patterns.  
The dataset (`students.csv`) includes attributes such as gender, parental education, study time, and test scores.  

The goal is to use SQL queries to identify the factors most associated with student success.

---

## 🎯 Objectives
- Is the length of stay the possible cause for mental health problem for international students?

---

## 🧰 Tools & Technologies
- **PostgreSQL** 💾  
- **DataCamp Workspace**  
- **CSV dataset:** `students.csv`  

---

## 📁 Data Structure

<img width="965" height="336" alt="image" src="https://github.com/user-attachments/assets/c886cc05-8000-4037-9f5a-6173fbe70efa" />



---

## 🧩 SQL Query

### 🔍  Length of stay a possible contributing factor for students mental health
```sql

SELECT stay,
	COUNT(*) AS count_int,
	ROUND(AVG(todep), 2) AS average_phq,
	ROUND(AVG(tosc), 2) AS average_scs,
	ROUND(AVG(toas), 2) AS average_as
FROM students
WHERE inter_dom = 'Inter'
GROUP BY stay
ORDER BY stay DESC
LIMIT 9;
```
## Result
<img width="933" height="276" alt="image" src="https://github.com/user-attachments/assets/97b2f021-a736-40d7-b584-e446a3bf9a86" />
---

