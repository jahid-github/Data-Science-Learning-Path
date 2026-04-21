# Data Engineering

Data engineers build and maintain the infrastructure that enables data to flow from source systems to storage, analysis, and ML models. This section covers the full modern data stack.

---

## Learning Steps

### 1. SQL & Databases (Foundation)
- Advanced SQL: window functions, CTEs, query optimization
- Relational: PostgreSQL, MySQL, SQL Server
- Analytical: BigQuery, Snowflake, Azure Synapse, DuckDB
- NoSQL: MongoDB (document), Redis (cache), InfluxDB (time-series)
- Vector DBs: Weaviate, Pinecone (needed for section 09 RAG systems)

### 2. Python for Data Engineering
- File formats: CSV, JSON, Parquet, Avro, Delta
- Data wrangling with Pandas, PySpark
- API consumption and web scraping
- Scheduling and automation with Python scripts

### 3. ETL / ELT Pipelines
- ETL vs ELT — when to transform before vs after loading
- Batch pipelines: extract → transform → load patterns
- Data modeling: Star Schema, Snowflake Schema, OBT
- dbt Core for SQL-based transformation layers
- Data quality and validation (Great Expectations)

### 4. Workflow Orchestration
- Apache Airflow: DAGs, operators, sensors, XComs
- Task dependencies, retries, SLAs, alerting
- Alternatives: Prefect, Dagster

### 5. Stream Processing
- Apache Kafka: topics, producers, consumers, partitions
- Apache Spark Structured Streaming
- MQTT for IoT/sensor data (aligned with robotics section)
- Use cases: real-time dashboards, fraud detection, event-driven ML

### 6. Cloud Data Platforms
- Azure: Data Lake Storage (ADLS), Data Factory (ADF), Synapse Analytics
- GCP: BigQuery, Cloud Storage, Dataflow, Pub/Sub
- Databricks: Delta Lake, Spark compute, Unity Catalog
- CI/CD for data pipelines: GitHub Actions

### 7. Containerization & Orchestration
- Docker: containerize pipelines and services
- Docker Compose: multi-service local environments
- Kubernetes: deploying and scaling data services
- NGINX: reverse proxy for data APIs

### 8. MLOps & Data Versioning
- MLflow: experiment tracking, model registry
- DVC: data versioning alongside Git
- Weights & Biases: experiment visualization

---

## Key Tools Summary

| Category | Tools |
|----------|-------|
| Orchestration | Apache Airflow, Prefect |
| Processing | Apache Spark, PySpark, dbt |
| Streaming | Apache Kafka, Spark Streaming |
| Storage | ADLS, Delta Lake, HDFS |
| Warehouse | BigQuery, Snowflake, Synapse, DuckDB |
| Cloud | Azure, GCP |
| Containers | Docker, Kubernetes |

---

## PDF Resources

### Platform and Command Line Tools

* [Azure CLI Cheat Sheet](./Azure_CLI_Cheat_Sheet.pdf)

### Data Preparation

* [Data Wrangling Cheat Sheet](./Data_Wrangling_Cheat_Sheet.pdf)

---

## Learning Resources

- [DataTalks.Club Data Engineering Zoomcamp](https://github.com/DataTalksClub/data-engineering-zoomcamp) — best free DE course
- [dbt Fundamentals](https://courses.getdbt.com/courses/fundamentals)
- [Databricks Academy](https://www.databricks.com/learn/training/home)
- [Kafka Quickstart](https://kafka.apache.org/quickstart)
