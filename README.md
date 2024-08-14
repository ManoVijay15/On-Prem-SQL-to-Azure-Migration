# On-Prem SQL to Azure Migration

## Project Overview

This project migrates an on-premises SQL database to Azure using Azure Data Factory (ADF), Databricks, Synapse Analytics, and Data Lake Storage. It involves setting up the environment, ingesting data, transforming it, and loading it into a serverless SQL database.

## Key Steps

1. **Data Ingestion**
   - **MySQL/SQL Server**:
     - Create pipelines in ADF to copy data from MySQL/SQL Server to Data Lake Storage.
     - Configure Key Vault for secrets.

2. **Data Transformation**
   - **Databricks**:
     - Set up a compute cluster.
     - Create notebooks to mount Data Lake Storage and transform data from Parquet to Delta format, and then from Silver to Gold.

3. **Data Loading**
   - **Synapse Analytics**:
     - Create a SQL database (`gold_db`) and SQL script to create serverless views.
     - Create a linked service and ADF pipeline to load data into Synapse.

## Prerequisites

- Azure Subscription
- Access to Azure Data Factory, Databricks, Synapse Analytics, and Data Lake Storage

## Troubleshooting

- Ensure SHIR is running and configured.
- Verify Databricks mount paths and permissions.
- Check ADF pipeline logs for errors.