# 🐝 Hive Queries & Results

This folder contains SQL queries executed on top of the MIMIC-III dataset using **Apache Hive**, along with visual results and table structure snapshots.

---

## 📄 Queries

Queries are stored in [`queries.sql`](./queries.sql).  
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

![Hive Tables](./results/hive_tables.png)

---

## 📊 Visual Results

| Query Description                      | Chart |
|----------------------------------------|--------|
| Average length of stay per diagnosis   | ![](./results/avg_length_stay.png) |
| Distribution of ICU readmissions       | ![](./results/icu_readmission.png) |
| Mortality by gender and age group      | ![](./results/mortality_gender_age.png) |

---

> All queries were run on external Hive tables linked to Parquet files stored in HDFS.
> Visualizations were created based on the query outputs using Python or plotting tools.
