# 🧮 MapReduce Job – Average Patient Age

This folder contains the Java-based MapReduce job used to calculate the **average patient age** from the `patients.csv` file in the MIMIC-III dataset.

---

## 📄 Files

| File | Description |
|------|-------------|
| [`java_script.txt`](./java_script.txt) | Java program (Mapper + Reducer) to calculate average patient age based on DOB and DOD. |
| `avg_age.jar` | *(Not included)* Compiled MapReduce job JAR (generated via `javac` + `jar`). |
| `Average-Age-Result.jpg` | Screenshot showing the job result output. |

---

## ⚙️ How to Run the Job

```bash
# Compile the Java code
export HADOOP_CLASSPATH=$(hadoop classpath)
javac -classpath $HADOOP_CLASSPATH -d avg_classes AverageAge.java
jar -cvf avg_age.jar -C avg_classes/ .

# Upload the input file to HDFS
hdfs dfs -mkdir -p /user/root/mimic
hdfs dfs -put /root/Patients.csv /user/root/mimic/

# Run the MapReduce job
hadoop jar avg_age.jar AverageAge /user/root/mimic/Patients.csv /user/root/output_avg
