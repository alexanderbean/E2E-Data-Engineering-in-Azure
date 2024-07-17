# Azure Data Factory - adf-e2e-de

Azure Data Factory was the tool used to engineer more of the extract/transform/load (ETL) pipeline.

**Extract:** I connected to the local SQL server database, queried for all of the tables, and copied them into the Bronze container in the data lake.

**Transform:** Then, I queued the Databricks notebooks to run and process the data from the Bronze to Silver layer and from the Silver to Gold layer.

**Load:** The load piece was completed by Azure Synapse Analytics, where it loaded the Gold container data into a serverless SQL database.

![adf-pipeline](https://github.com/user-attachments/assets/124ab5d1-e781-4229-9f0b-3dce0bc3806f)
