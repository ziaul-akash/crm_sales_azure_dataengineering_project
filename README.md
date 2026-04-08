
CRM_SALES_UKSOUTH_AZURE_PROJECT_DETAILS
---------------------------------------------

A real-world, end-to-end Azure Data Engineering pipeline built on CRM sales data — covering ingestion, transformation, security, analytics, and visualisation using industry-standard Azure services.


Overview:
-------------
This project demonstrates a complete modern data engineering workflow on Microsoft Azure. Starting from on-premises CSV/CRM data, the pipeline ingests, transforms, secures, and serves data all the way through to interactive Power BI dashboards. It is designed as a portfolio-quality project for data engineers preparing for cloud roles or Azure certifications.

Architecture:
---------------
The diagram illustrates the full pipeline. Data flows from on-premises sources through Azure Data Factory into a two-zone Data Lake (raw → curated), is transformed by Databricks, analysed via Synapse Analytics, and visualised in Power BI. Security is enforced end-to-end using Azure Key Vault and Databricks Secret Scope. Reliability is handled by Logic Apps email alerts and Azure Monitor.


What We Will Do:
----------------

1. On-premises to cloud ingestion — move local CSV/CRM data into Azure using ADF with a Self-Hosted Integration Runtime, enabling secure connectivity without exposing internal systems directly.
2. Git-integrated pipeline development — connect ADF to a Git repository for version control, branching, and enterprise-grade collaborative development.
3. Data Lake architecture — structure Azure Data Lake Storage Gen2 into raw and curated zones following the medallion pattern, with separate containers per data domain.
4. Pipeline reliability — configure Azure Logic Apps to send automated email notifications on pipeline success or failure, and use Azure Monitor for detailed operational tracking.
5. Data transformation with Databricks — write PySpark notebooks to clean, standardise, and enrich raw CRM data before writing to the curated zone.
6. Secrets management — store sensitive credentials (storage keys, connection strings) in Azure Key Vault and mount them into Databricks via a Secret Scope, keeping secrets out of code entirely.
7. SQL analytics on the Data Lake — use Azure Synapse Analytics to run serverless SQL queries directly against Parquet/Delta files in the curated zone, without loading data into a warehouse.
8. Business intelligence — connect Power BI to Synapse Analytics and build interactive dashboards to surface sales insights for business stakeholders.
7. SQL analytics on the Data Lake — use Azure Synapse Analytics to run serverless SQL queries directly against Parquet/Delta files in the curated zone, without loading data into a warehouse.
8. Business intelligence — connect Power BI to Synapse Analytics and build interactive dashboards to surface sales insights for business stakeholders.
