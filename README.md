# 🚀 End‑to‑End Azure Data Engineering Project | Car Sales Analytics

This project showcases a **production‑style end‑to‑end Azure Data Engineering pipeline** built for **Car Sales Analytics**, implementing real‑world data engineering patterns using **Azure Data Factory** and **Azure Databricks**.

The solution demonstrates how raw data is ingested, incrementally processed, transformed using the **Medallion Architecture**, and modeled into an **analytics‑ready Star Schema**, following enterprise best practices.

## 🔹 Project Flow Summary

*   Car sales data is copied from **GitHub** into **Azure SQL Database**, which acts as the transactional source system
*   **Azure Data Factory (ADF)** handles ingestion, incremental loading, and orchestration
*   **Azure Databricks** performs data transformations across Bronze, Silver, and Gold layers
*   Final output is a **Fact\_Sales table and Dimension tables** optimized for analytics

## 🔹 Azure Data Factory Pipelines

*   **SourcePrep Pipeline**  
    Copies car sales data from GitHub into Azure SQL Database

*   **IncremDataPipeline**  
    Performs incremental data loads from Azure SQL to Azure Data Lake using the **watermark pattern**  
    (lookup last/current load → copy activity → stored procedure update)

*   **DBNotePipeline**  
    Triggers Azure Databricks notebooks from ADF for data processing

*   **MasterPipeline**  
    Orchestrates the complete end‑to‑end workflow:  
    `SourcePrep → IncremDataPipeline → DBNotePipeline`
    
## 🔹 Data Transformation (Azure Databricks)

*   Implemented **Medallion Architecture**
    *   **Bronze** – Raw incremental data
    *   **Silver** – Data cleansing, standardization, and business transformations
    *   **Gold** – Analytics‑ready tables
*   Built **Fact\_Sales** and **Dimension tables** using **Star Schema**
*   Implemented **SCD Type‑1 (upsert logic)** on dimension tables
*   Used **Delta Lake** for ACID transactions, reliability, and performance
  
## 🔹 Governance & Version Control

*   **Unity Catalog** used for schema management and access governance
*   Databricks notebooks integrated with **GitHub (Repos)**
*   GitHub acts as the central repository for notebooks and raw data files
  
## ⭐ Key Highlights

*   End‑to‑end orchestration using ADF **MasterPipeline**
*   Incremental data loading via **watermark pattern**
*   SCD Type‑1 implementation on dimension tables
*   Clear separation of **Silver (transformations)** and **Gold (analytics)** layers
*   Databricks notebooks triggered directly from ADF
*   Fully **Git‑integrated** development workflow
*   Analytics‑ready **Star Schema** design

## 🧰 Tech Stack

**Azure Data Factory | Azure Databricks | Azure SQL Database | ADLS Gen2 | Delta Lake | Unity Catalog | PySpark | SQL | GitHub**
