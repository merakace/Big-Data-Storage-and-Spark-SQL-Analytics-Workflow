# Big Data Storage and Spark SQL Analytics Workflow

**Curriculum anchor:** 25MSDA3S01 – Big Data Analytics  
**Pillar:** Market & AI skill  
**Hiring round simulated:** AI workflow assessment

## Objective
Build a local Spark analytics workflow that loads a retail dataset, stores it as a Hive-compatible catalog table, executes analytical queries using Spark SQL, visualizes aggregated metrics, and measures query execution time.

## Repository structure
```text
big_data_spark_sql_analytics/
├── data/
│   └── retail_orders.csv
├── outputs/
│   ├── city_revenue_summary_reference.csv
│   ├── category_performance_reference.csv
│   ├── order_status_summary_reference.csv
│   ├── city_revenue_reference.png
│   ├── monthly_revenue_reference.png
│   └── category_revenue_reference.png
├── Big_Data_Spark_SQL_Analytics.ipynb
├── requirements.txt
└── README.md
```

## Dataset
A deterministic synthetic retail orders dataset with 1,200 rows and fields for order ID/date, customer ID, city, product category, sales channel, quantity, unit price, discount, order status, delivery days and customer rating. It is generated for learning and does not contain real customer data.

## Requirements
- Python 3.9+
- Java compatible with your installed Spark version
- PySpark
- Pandas
- Matplotlib
- Jupyter Notebook

Install packages:
```bash
python -m pip install -r requirements.txt
```

Open the notebook and run cells from top to bottom:
```bash
jupyter notebook
```

## Workflow
1. Create a local Spark session with Hive support.
2. Read the CSV dataset into a Spark DataFrame.
3. Prepare date, gross amount and net amount fields.
4. Create a database and save a Parquet-backed table in the Spark catalog.
5. Run Spark SQL queries for city revenue, category performance, monthly revenue, order status and top cities by category.
6. Visualize aggregated query outputs.
7. Measure query execution times and inspect a formatted physical plan.
8. Export query outputs and timing results.

## Hive integration clarification
The notebook enables Hive support and stores a table in the local Spark catalog/warehouse. This is a local Hive-enabled demonstration, not proof of connection to a separate enterprise Hive Metastore. For a shared Hive deployment, configure `hive-site.xml`, the metastore URI, compatible Hive libraries, and access permissions before starting Spark.

## Performance note
Execution times are collected on the machine running the notebook and are affected by hardware, Java/Spark versions, cache state and startup overhead. They should not be presented as cluster benchmarks.

## Tools
Apache Spark, PySpark, Spark SQL, Hive integration, Python, Pandas, Matplotlib, Jupyter Notebook.
