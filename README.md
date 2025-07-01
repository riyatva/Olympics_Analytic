# Olympics_Analytic
End-to-end Azure Data Engineering project analyzing Olympic datasets using ADF, Databricks, Synapse, and Power BI.


# Olympic Data Analytics – Azure End‑to‑End Data Engineering Project

One of the largest data engineering use-cases: from fetching raw Olympic datasets up to building Power BI dashboards, all powered by Azure!

## 🚀 Tech Stack

- **Azure Data Factory** – for orchestrating data ingestion pipelines  
- **Azure Data Lake Storage Gen2** – raw “bronze” and curated “silver” data landing zones  
- **Azure Databricks (PySpark)** – for cleaning, transforming, and enriching data  
- **Azure Synapse Analytics** – serverless SQL pools for scalable querying  
- **Power BI** – interactive dashboards for storytelling

## 🛠️ Architecture Overview

Describe pipeline stages and include `architecture/azure_pipeline.png`.

1. **Data Ingestion**  
   - ADF copies raw CSVs from a public Github`/bronze/`.
2. **Data Transformation**  
   - Databricks mounts ADLS, ingests data → applies cleans, schema enforcement → writes to `/silver/`.
3. **Data Modeling & Querying**  
   - Synapse loads curated data, optimized tables/views created.
4. **Visualization**  
   - Power BI consumes Synapse tables for interactive dashboards.

## 📂 Getting Started

### Prerequisites
- Azure ( Free account would also work ) + access to create Data Factory, Databricks, Synapse, ADLS.
- [Azure CLI](https://learn.microsoft.com/cli/azure/install-azure-cli), or Azure Portal access.
- Power BI Desktop installed.

### Setup

1. **Clone the repository**  
   ```bash
   git clone https://github.com/your-username/olympic-data-analytics-azure.git
   cd olympic-data-analytics-azure
   Create Azure resources

2.Use pipelines/arm-templates or Terraform scripts to provision Data Factory, Storage, Databricks, Key Vault, Synapse.

Upload raw datasets

3.Download from Kaggle (e.g. athletes.csv, teams.csv, etc.) and upload to ADLS /bronze/.

Deploy ADF pipelines

4.Import JSON definitions from pipelines/ via ADF UI or CLI.

Run Databricks notebooks

5.Open notebooks under notebooks/, adjust mount paths/secrets, run to transform and save to /silver/.

Setup Synapse SQL Pools

6.Run scripts from sql/ to create tables/views on transformed data.

7.Load Power BI Dashboard

Open .pbix file in powerbi/, configure Synapse connection, explore insights.


📈 Key Learnings
End-to-end data pipeline automation

Secure mounting ADLS in Databricks using Azure AD and secrets

Modular "Bronze → Silver → Gold" medallion data architecture

Seamless connectivity across Azure services

Building an interactive dashboard with Power BI



