# 🧮 MapReduce Job – Average Patient Age

This folder contains the Java-based MapReduce job used to calculate the **average patient age** from the `patients.csv` file in the MIMIC-III dataset.

> This is part of a larger healthcare data pipeline project using the MIMIC-III dataset. The goal of this task is to perform distributed computation (MapReduce) to extract insights from patient records.

---

## 📄 Files

| File | Description |
|------|-------------|
| [`AverageAge.java`](./java_script.txt) | Java program (Mapper + Reducer) |
| `avg_age.jar` | Compiled MapReduce job JAR |

---

## ⚙️ How to Run the Job

```bash
# 1. Compile
export HADOOP_CLASSPATH=$(hadoop classpath)
javac -classpath $HADOOP_CLASSPATH -d avg_classes AverageAge.java
jar -cvf avg_age.jar -C avg_classes/ .

# 2. Upload to HDFS
hdfs dfs -mkdir -p /user/root/mimic
hdfs dfs -put /root/Patients.csv /user/root/mimic/

# 3. Execute
hadoop jar avg_age.jar AverageAge /user/root/mimic/Patients.csv /user/root/output_avg

# 4. View Results
hdfs dfs -cat /user/root/output_avg/part-r-00000
