# 🚀 Spark Week 6 Assignment

## 📌 Overview
This project demonstrates key concepts of Apache Spark using an **e-commerce transactions dataset**.  
It covers reading data, transformations, actions, optimizations, and storage formats.

---

## 🔑 Concepts Covered
- **Driver, Cluster Manager, Executor** roles
- **Lazy Evaluation** and DAG optimization
- **Schema inference** with CSV
- **CSV vs Parquet** storage formats
- **Transformations vs Actions**
- **Lineage Graph (DAG)** for fault tolerance
- **Predicate Pushdown** in Parquet
- **Client Mode vs Cluster Mode**

---

## 🛠️ Steps Implemented
1. **Setup SparkSession**  
   ```python
   from pyspark.sql import SparkSession
   spark = SparkSession.builder.appName("Week6_Assignment").getOrCreate()
   ```

2. **Load Dataset (CSV)**  
   ```python
   df = spark.read.option("header", "true").option("inferSchema", "true").csv("ecommerce_transactions.csv")
   df.printSchema()
   df.show(5)
   ```

3. **Filtering & Selection**  
   - Electronics transactions  
   - Payment method filters  
   - Country-based filters  

4. **Column Operations**  
   - Rename columns  
   - Type casting  
   - Derived column (`Final_Price` with tax)

5. **Null Handling**  
   - Filter out null `User_Name` values  

6. **Storage Format Conversion**  
   - Write to **Parquet**  
   - Read back and export cleaned data to **CSV**

7. **Performance Comparison**  
   - Measured filter times on CSV vs Parquet  
   - Parquet consistently faster due to **predicate pushdown**

---

## 📊 Key Insights
- **Lazy evaluation** ensures Spark optimizes the entire pipeline before execution.  
- **Parquet** outperforms CSV for columnar queries.  
- **Fault tolerance** is achieved via recomputation using lineage graphs.  
- **.show(5)** is safer than `.collect()` for large datasets.  
- Dataset checks revealed:
  - No purchases > 1000 (max ~999.98).  
  - No nulls in `User_Name`.  

---

## ✅ Summary
This notebook demonstrates a **full Spark pipeline**:
- Read → Transform → Filter → Write  
- Showcases Spark’s optimizations, fault tolerance, and performance benefits of Parquet over CSV.  

