# 🧮 MapReduce Job – Average Patient Age

This folder contains the Java-based MapReduce job used to calculate the **average patient age** from the `patients.csv` file in the MIMIC-III dataset.

---

## 📄 Files

| File | Description |
|------|-------------|
| [`AverageAge.java`](./AverageAge.java) | Java program with Mapper and Reducer to compute average age from patient DOB and DOD. |
| `avg_age.jar` | Compiled JAR file (generated via `javac` + `jar`). |
| `results/avg_age_output.png` | Screenshot showing the output (e.g., average age = 70.6). |

---

## ⚙️ How to Run

```bash
# Compile the Java code
export HADOOP_CLASSPATH=$(hadoop classpath)
javac -classpath $HADOOP_CLASSPATH -d avg_classes AverageAge.java
jar -cvf avg_age.jar -C avg_classes/ .

# Upload input data to HDFS
hdfs dfs -mkdir -p /user/root/mimic
hdfs dfs -put /root/Patients.csv /user/root/mimic/

# Run the MapReduce job
hadoop jar avg_age.jar AverageAge /user/root/mimic/Patients.csv /user/root/output_avg
