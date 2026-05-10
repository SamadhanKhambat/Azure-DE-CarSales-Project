
🚀 End-to-End Azure Data Engineering Project | Car Sales Analytics

📌 Overview

Built a production-style Azure Data Engineering pipeline using Azure Data Factory, Azure Databricks, ADLS Gen2, Delta Lake, and Unity Catalog following Medallion Architecture (Bronze, Silver, Gold).

⚙️ Tech Stack

Azure Data Factory | Azure Databricks | PySpark | Delta Lake | ADLS Gen2 | Azure SQL | Unity Catalog | GitHub | SQL

🔄 Project Flow

Loaded car sales data from GitHub into Azure SQL
Implemented incremental loading using Watermark Pattern in ADF
Ingested raw data into Bronze layer
Applied cleansing and transformations in Silver layer
Built Fact & Dimension tables in Gold layer using Star Schema
Implemented SCD Type-1 Upsert logic using Delta Lake
Orchestrated end-to-end workflow using ADF MasterPipeline
Integrated Databricks notebooks with GitHub for version control


✅ Key Features

Incremental Data Loading
Medallion Architecture
Delta Lake Merge Operations
SCD Type-1 Implementation
Star Schema Modeling
Unity Catalog Governance
End-to-End ADF Orchestration


📂 Pipelines

SourcePrepPipeline
IncremDataPipeline
DBNotePipeline
MasterPipeline
