# 📁 MIMIC-III Dataset

This folder contains a selection of raw CSV files extracted from the MIMIC-III Clinical Database.  
These files are the **starting point** of the pipeline — before any cleaning or transformation.

---

## 📄 Files Overview

| File | Description |
|------|-------------|
| **patients.csv** | Demographic information like gender, date of birth, and death. Each row = one patient. |
| **admissions.csv** | Admission-level info like admission time, type, discharge time, and death flag. |
| **icustays.csv** | ICU-specific admissions with in/out times and duration of stay. |
| **diagnoses_icd.csv** | Diagnoses during admissions, coded using ICD (International Classification of Diseases). |

---

## ✅ Why These Files?

These four files were chosen because they offer a good base for analytics like:
- Patient age calculation
- ICU admission patterns
- Mortality analysis
- Disease frequency (via ICD codes)

---

## 📝 Notes

- These are raw CSVs directly from the original MIMIC-III dump.
- No cleaning or formatting was applied here.
- Cleaned and transformed versions are available under [`Cleaned_Data/`](../Cleaned_Data/).

---

## 🔗 Source

Original dataset available from [PhysioNet](https://mimic.physionet.org/).  
Usage requires credentialed access and agreement to the data license.

---

## 📦 About MIMIC-III

MIMIC-III (Medical Information Mart for Intensive Care) is a large, publicly available database of de-identified health data from ICU patients. It contains 50+ tables including labs, procedures, prescriptions, notes, etc.

Only a subset of this dataset was used in this project based on relevance.

🔗 Full schema and table descriptions are available at:  
[https://mimic.mit.edu/docs/iii/](https://physionet.org/content/mimiciii-demo/1.4/)



