# e2e-de-azure

This is my first data engineering project and my first non-academic project.

I created an end-to-end pipeline from an on-prem SQL Server Database

I connected Azure Data Factory, Azure Databricks, and Synapse Analytics to this Git repository for audit records and to have a centralized location to run processes from.

The extract/transform/load pipeline accesses and runs the notebooks from "/databricks-notebooks"

The dataset used was the Microsoft lightweight AdventureWorksLT2022 set: https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver16&tabs=ssms

My goal in this project was to learn more about the development stages in a data engineering pipeline, and to gain hands-on practice with the Azure cloud platform and its many tools.

In this project, I used:

Azure Gen2 Data Lake Storage
Azure Data Factory
Azure Databricks
Microsoft SQL Server
Azure SQL Database
SQL Server Management Studio
Power BI Desktop
These are the major steps I took in creating this end-to-end project:

I created the resource group to house the applicable deployed services listed above.
I added three BLOB storage containers in Azure Gen2 Data Lake Storage for staging, raw, and transformed data.
I imported data from local .csv files into the staging data container.
In Data Factory, I developed a pipeline to copy the staging data into the raw data container.
Transformed the raw data in Databricks using pySpark and some imported SQL functions. I then saved this new data into the transformed data container.
In SSMS, I assigned the table schemas for the transformed data to enable me to develop the final load pipeline.
Back in Data Factory, I developed a pipeline to load the transformed data from BLOB storage into Azure SQL Database (hosted in Microsoft SQL Server).
I then connected to the Azure SQL Database data in Power BI Desktop and conducted basic analysis and data visualization.
Then published the dashboards to the Power BI service.
I established a Git repo connection to Data Factory after all the pipelines were completed.
