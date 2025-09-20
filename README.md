Databricks End-to-End Data Engineering Pipeline
📌 Overview

This project demonstrates an end-to-end data engineering pipeline using Azure Databricks and Apache Spark.
The pipeline simulates a real-world ETL flow: ingesting data from parquet files, transforming & cleaning it, enriching with joins, and producing aggregated outputs stored back in parquet format.

⚡ Note: This project was originally developed and tested during my Azure Databricks trial account. Since the trial expired, the code is shared here as a reference. It can still be executed on Databricks Community Edition or locally with PySpark.

🛠 Tech Stack

i. Azure Databricks (Spark cluster management, notebooks)

ii. Apache Spark / PySpark (ETL transformations)

iii. Delta/Parquet (data storage formats)

🔄 Pipeline Steps

1.) Data Ingestion

Loaded sample parquet files: customers, orders, products, and regions.

2.)Data Transformation

Performed joins across customers, orders, and products to enrich data.

Cleaned records with missing values.

Applied aggregations: e.g., total sales by region/product.

3.)Data Storage

Saved transformed datasets back into parquet format.

Output can be used for reporting / dashboards.

📂 Repository Structure
📁 databricks-etl-pipeline
 ┣ 📄 notebook.dbc        # Main Databricks notebook (exported)
 ┣ 📄 README.md           # Project documentation
 ┗ 📂 data/ (optional)    # Sample parquet files (if uploaded)

🚀 How to Run
Option 1: Run on Databricks

Create a Community Edition account: https://community.cloud.databricks.com

Import the notebook.dbc.

Upload sample parquet files to DBFS.

Run notebook cells sequentially.

Option 2: Run Locally with PySpark

i. Install PySpark:
pip install pyspark

ii. Replace dbfs:/ paths with local paths (./data/filename.parquet).

iii. Run the script / notebook on local Spark.

📈 Future Improvements

a. Add incremental data loading logic.

b. Integrate Delta Lake for versioned data.

c. Orchestrate with Airflow / ADF.

d. Connect to Power BI for visualization.

🙌 Acknowledgement
Inspired by Ansh Lamba’s Databricks End-to-End project. Extended & adapted for learning purposes.
