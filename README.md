🧠 SQL Data Warehouse Project (ETL + Modeling + Architecture)

Welcome to my SQL Data Warehouse Project! 🚀
This repository showcases a full end-to-end Data Warehouse built from scratch — including ETL development, data modeling, architecture design, and clean repository structuring.

The project is designed as a practical portfolio piece to demonstrate real-world data engineering practices using only SQL Server.


---

🏗 Medallion Data Architecture

This Data Warehouse follows the Medallion Architecture, organizing data into three structured layers:


---

🔹 1. Bronze Layer – Raw Data Ingestion

Stores raw source data exactly as received.

Source: CSV files extracted from CRM & ERP systems.

Loaded into SQL Server using structured ingestion scripts.

Ensures:

Full data lineage

Traceability

Load-time tracking

Row count validation

---

🔸 2. Silver Layer – Transformation & Standardization

Cleans, validates, and standardizes raw data.

Implements business rules to unify definitions across all sources.

Transformation logic developed using T-SQL.

Includes:

TRY...CATCH for error handling

Logging tables to track ETL execution

Duplicate handling, NULL fixes, and type standardization


Prepares the data for analytical modeling.



---

🏆 3. Gold Layer – Business-Ready Data Model

Builds Fact and Dimension tables following a Star Schema.

Contains final curated, analytics-ready datasets.

Includes:

Business KPIs & metrics

Hierarchies

Flattened reporting tables for optimized BI performance


Used for reporting, dashboards, and advanced analytics.



---

⚙️ ETL Process Overview

The entire ETL pipeline is implemented using SQL Stored Procedures and follows the Bronze → Silver → Gold process:

Extraction

Load raw CSV source files into Bronze.


Transformation

Apply data cleaning, normalization, and business rules.


Loading

Move curated datasets into Silver & Gold layers.


✔ Key ETL Features:

Error handling with TRY...CATCH

Row count checks for data integrity

Execution logging for auditing

Automated workflow using stored procedures



---

🧩 Data Modeling

The Gold Layer is built using a Star Schema:

Fact Tables

Store measurable events (sales, orders, transactions).


Dimension Tables

Hold descriptive business context (customers, products, dates).



Includes:

Surrogate keys

Primary–foreign key relationships

Lookup references

Fully normalized dimensions


A complete data model diagram is included in this repository.


---

🪄 Logging & Monitoring

To ensure traceability and auditability:

Each ETL step logs:

Timestamps

Row counts

Execution status

Error messages (if any)


Designed for easy debugging and ETL monitoring.



---

📁 Repository Structure

📂 SQL-Data-Warehouse-Project
 ┣ 📂 Datasets/               → Raw CSV files (CRM & ERP)
 ┣ 📂 Scripts/
 ┃   ┣ 📂 Bronze/            → Ingestion procedures
 ┃   ┣ 📂 Silver/            → Cleaning & transformation procedures
 ┃   ┗ 📂 Gold/              → Fact & dimension modeling scripts
 ┣ 📂 Diagrams/              → Architecture & Star Schema (draw.io)
 ┣ 📂 Documentation/         → Data dictionary & business rules
 ┗ 📄 README.md              → Project overview (this file)


---

🧰 Tools & Technologies

SQL Server – Database & ETL execution

T-SQL Stored Procedures – Transformation logic

draw.io – Architecture & modeling diagrams

CSV / Excel – Source data

GitHub – Version control & project documentation

-------

🔮 Future Improvements

This project will be re-implemented using:

Python

Apache Airflow


to build a fully orchestrated, automated modern data pipeline.
