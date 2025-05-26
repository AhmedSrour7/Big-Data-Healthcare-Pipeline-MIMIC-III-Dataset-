# 🐝 Hive Queries & Results

This folder contains SQL queries executed on top of the MIMIC-III dataset using **Apache Hive**, along with visual results and table structure snapshots.

---

## 📄 Queries

Queries are stored in [Hive_queries](./Hive/"hive queries.txt").  
Key topics covered:

- Most common ICD diagnoses
- ICU readmission rate
- Mortality statistics by gender and age
- Admission types distribution
- Average length of stay per diagnosis

---

## 🧱 Hive Tables Overview

The following external tables were created in Hive using the cleaned Parquet files:

- `patients`
- `admissions`
- `icustays`
- `diagnoses_icd`

📸 Below is a snapshot of the table structures:

![Hive Tables](./Hive%20Results/Hive-tables.png)

---

## 📊 Visual Results

| Query Description                      | Chart |
|----------------------------------------|--------|
| Average length of stay per diagnosis   |![](./Hive%20Results/Average%20length%20of%20stay%20per%20diagnosis.png) |
| Distribution of ICU readmissions       |![](./Hive%20Results/Distribution%20of%20ICU%20readmissions.png) |
| Mortality by gender and age group      |![](./Hive%20Results/Mortality%20rates%20by%20demographic%20groups.png) |

---

> All queries were run on external Hive tables linked to Parquet files stored in HDFS.
> Visualizations were created based on the query outputs using Python or plotting tools.
