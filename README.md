# Customer Analytics: Preparing Data for Modeling

![Two data scientists working on a dashboard.](hr-image-small.png)

A common challenge when building predictive models for business applications is the size of the datasets. Large datasets can slow down training and prediction, sometimes taking days to complete. By optimizing storage and data types, we can drastically improve efficiency without sacrificing valuable information.

In this project, I worked with a dataset from *Training Data Ltd.*, aimed at predicting whether students were looking for a new job. The goal was to transform the dataset into a more memory-efficient version while preserving its analytical value.

---

## 📌 Guiding Questions
- How can we efficiently store large datasets by optimizing data types?  
- What categorical columns should be stored as **ordered categories** vs. **nominal categories**?  
- How much memory can we save by converting columns to their most efficient types?  
- After preprocessing, which students (with ≥10 years of experience and working in large companies) should be retained in the final dataset?

---

## 📂 The Data
### **customer_train.csv**

| Column                   | Description                                                                      |
|---------------------------|----------------------------------------------------------------------------------|
| `student_id`             | A unique ID for each student.                                                    |
| `city`                   | A code for the city the student lives in.                                        |
| `city_development_index` | A scaled development index for the city.                                         |
| `gender`                 | The student's gender.                                                            |
| `relevant_experience`    | An indicator of the student's work relevant experience.                          |
| `enrolled_university`    | The type of university course enrolled in (if any).                              |
| `education_level`        | The student's education level.                                                   |
| `major_discipline`       | The educational discipline of the student.                                       |
| `experience`             | The student's total work experience (in years).                                  |
| `company_size`           | The number of employees at the student's current employer.                       |
| `company_type`           | The type of company employing the student.                                       |
| `last_new_job`           | The number of years between the student's current and previous jobs.             |
| `training_hours`         | The number of hours of training completed.                                       |
| `job_change`             | Whether the student is looking for a new job (`1`) or not (`0`).                 |

---

## 🛠️ How I Approached the Project

1. **Exploratory Data Analysis (EDA)**  
   - Explored `customer_train.csv` to identify column types and their optimal storage formats.  

2. **Converting Integers, Floats, and Categories**  
   - Converted integers → `int32`  
   - Converted floats → `float16`  
   - Converted two-factor categories → `bool`  
   - Converted nominal categories → `category`  

3. **Handling Ordered Categories**  
   - Transformed ordinal categorical columns (e.g., `experience`, `education_level`) into ordered categories to preserve their hierarchy.  

4. **Filtering Data**  
   - Filtered the DataFrame to retain only students with ≥10 years of experience at companies with ≥1000 employees.  

---

## ✅ Key Deliverables
- Performed **data type optimization** to minimize memory usage.  
- Converted **categorical data** into efficient formats (nominal vs. ordered).  
- Applied **Boolean encoding** for binary columns.  
- Filtered dataset for **senior professionals in enterprise companies**.  
- Demonstrated substantial **reduction in dataset memory usage**.  

---

## 🧰 Skills Used
- Python (`pandas`, `numpy`)  
- Data cleaning & preprocessing  
- Efficient data type conversion  
- Handling categorical & ordinal data  
- Memory optimization in large datasets  
