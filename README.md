End-to-End Data Engineering Pipeline with Azure Databricks
📌 Overview

This project demonstrates an end-to-end data engineering pipeline built using Azure Databricks and Apache Spark.
The pipeline simulates a real-world ETL flow: ingesting data from parquet files, transforming & cleaning it, enriching with joins, and producing aggregated outputs stored back in parquet format.

⚡ Note: This project was developed during an Azure Databricks trial account. Code can be run on Databricks Community Edition or locally using PySpark.

🛠 Tech Stack
i. Azure Databricks (notebooks & cluster management)
ii. Apache Spark / PySpark (ETL transformations)
iii. Delta/Parquet (data storage)

🔄 Pipeline Steps
a. Data Ingestion
Load sample parquet files: customers, orders, products, and regions.
b. Data Transformation
Join datasets to enrich orders with customer & product info.
Clean null or invalid records.
Apply aggregations (e.g., total sales by region/product).
c. Data Storage
Save transformed datasets in parquet format.
Ready for downstream reporting or dashboarding.

📂 Repository Structure
📁 End-to-End-Data-Engineering-Pipeline-with-Azure-Databricks
 ┣ 📂 notebooks_dbc/         # Original Databricks notebooks
 ┃   ┗ 📄 etl_pipeline.dbc
 ┣ 📂 notebooks_py/          # Exported .py notebooks for readability
 ┃   ┣ 📄 bronze_layer.py
 ┃   ┣ 📄 silver_layer.py
 ┃   ┗ 📄 gold_layer.py
 ┣ 📂 data/                  # Sample parquet datasets
 ┃   ┣ 📄 customers_sample.parquet
 ┃   ┗ 📄 orders_sample.parquet
 ┣ 📄 README.md              # Project documentation
 ┣ 📄 .gitignore             # Ignores cache, logs, and large files
 ┗ 📄 requirements.txt       # Project dependencies

🚀 How to Run
Option 1: On Databricks
i. Sign up for Community Edition: https://community.cloud.databricks.com
ii. Import notebooks from notebooks_dbc/.
iii. Upload sample parquet files to DBFS (optional small subset).
iv. Run notebook cells sequentially.

Option 2: Locally with PySpark
i. Install PySpark:
ii. pip install -r requirements.txt
iii. Replace DBFS paths with local paths (e.g., data/customers_sample.parquet).
iv. Run .py notebooks/scripts using Python.

📈 Future Improvements
Incremental data loading & ETL automation
Delta Lake for versioned data
Orchestration using Airflow or Azure Data Factory
Connect to Power BI / dashboards for reporting

🙌 Acknowledgements

Inspired by Ansh Lamba’s Databricks End-to-End Project; adapted for learning purposes and portfolio use.
