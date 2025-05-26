# 🗂️ MIMIC-III Dataset (Extracted Files)

This folder contains selected and preprocessed CSV files from the **MIMIC-III Clinical Database**, which were used in the Big Data Healthcare Analytics Pipeline project.

---

## 📊 Files Description

| File Name           | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| `patients.csv`      | Contains demographic details of patients (gender, date of birth, death...). |
| `admissions.csv`    | Records hospital admissions including admission type, time, and discharge.  |
| `icustays.csv`      | ICU-specific admission records and ICU stay durations.                      |
| `diagnoses_icd.csv` | Medical diagnoses associated with admissions using ICD codes.               |

---

## 🧾 Notes

- These files are raw (unmodified) extracts from the original MIMIC-III dataset.
- Used as inputs for data cleaning and further processing using Python + pandas.
- Files were later converted to **Parquet format** and stored in HDFS for querying via Hive.

---

## ⚠️ Licensing

The full MIMIC-III dataset is available upon request from [PhysioNet](https://mimic.physionet.org/).  
These CSV files are shared here only as part of academic demonstration and **do not contain sensitive information**.

