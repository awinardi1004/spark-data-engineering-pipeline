# End-to-End Big Data Pipeline with Apache Spark & Hadoop
## 📌 Project Overview
This project demonstrates the implementation of an end-to-end big data pipeline using Apache Spark and Hadoop (HDFS) with the [Olist E-commerce dataset](https://github.com/awinardi1004/spark-data-engineering-pipeline/tree/main/data_source).

The pipeline covers the full data engineering workflow:
1. Data ingestion & exploration
2. Data cleaning & transformation
3. Data integration & aggregation
4. Property optimization (join strategies & caching)
5. Data serving (outputs stored in HDFS as Parquet/CSV)

## 🛠️ Technologies Used
* Apache Hadoop (HDFS) → distributed storage
* Apache Spark (PySpark) → distributed data processing
* Jupyter Notebook → development & documentation
* Parquet & CSV → storage formats

## 🔄 Workflow
1. Data Ingestion & Exploration
* Loaded raw CSV data from HDFS into Spark.
* Inspected schema, record counts, and performed initial exploration.
* dentified data issues (nulls, duplicates, type mismatches, missing values).

2. Data Cleaning & Transformation
* Standardized zip_code_prefix (int → string).
* Removed duplicates in geolocation dataset.
* Imputed missing product dimensions (weight, height, width, length).
* Escalated unsolvable issues (invalid delivery dates, high missing review comments).
* Saved cleaned parquet files in HDFS.
3. Data Integration & Aggregation
* Joined multiple tables into full_orders_df.
* Generated business insights:
* Total orders per customer
* Average review score per seller
* Top 10 most sold products
* Top customers by spending
* Stored processed parquet files in HDFS.

4. Property Optimization
* Applied join strategies (Broadcast Join, Sort-Merge Join, Bucket Join).
* Implemented caching to optimize repeated queries.

## 📊 Outputs / Results
* Cleaned & standardized datasets stored as Parquet in HDFS.
* Integrated dataset (full_orders_df) containing enriched business metrics.
* Optimized queries (broadcast join & caching reduced execution time).
* Data ready for BI dashboards and ML use cases.

## 📌 Key Takeaways
* Built a scalable end-to-end data engineering pipeline.
* Learned how to optimize Spark jobs with caching and join strategies.
* Demonstrated how raw messy data can be transformed into analytics-ready datasets.