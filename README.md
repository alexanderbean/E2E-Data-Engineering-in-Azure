# End-to-End ETL Pipeline in Microsoft Azure - (e2e-de-azure)

This is my first complete end-to-end data engineering project. In this project, I created an end-to-end ETL pipeline starting from an on-prem SQL Server Database, moving into the Azure cloud, and ending with a Power BI dashboard/report.

My goals for this project were:
- To gather a general understanding of what makes a data engineering pipeline,
- To gain hands-on experience with the Azure cloud platform and offered services, and
- To produce a functional and stable end product to showcase on GitHub and my resume.

The dataset used was one of the Microsoft sample datasets: [AdventureWorksLT2022](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorksLT2022.bak)
![azurediagram2](https://github.com/user-attachments/assets/c84689e4-8ff1-4894-82eb-f295b5741952)

# Project Steps

On-Prem SQL Server Database:
- Before starting on the cloud, I installed SQL Server Express to host the local server and set up SQL Server Management Studio.
- I also downloaded the Java Runtime Environment (JRE) to support the Parquet format.

Github:
- I created this repository to track the progression of the project.
- When Azure Data Factory, Azure Databricks, and Azure Synapse Analytics were created: I completed Git configuration within the instances so any changes or publishes were pushed to a branch for easy audit/documentation.

Microsoft Azure:
- Once in Azure, I established the resource group to house all the resources for the project.
- I then created the following resources: Azure Data Lake Storage Gen2, Azure Key Vault, Azure Data Factory (ADF), Azure Databricks, and Azure Synapse Analytics.
- Azure Data Lake Storage Gen2: I created the storage containers for the Bronze, Silver, and Gold layers.
- Azure Key Vault: I assigned secrets to the login and password of the local SQL database to be used in linked services in Azure Data Factory.
- Azure Data Factory (ADF): I engineered the pipelines to extract the data from the on-prem database and to execute the Databricks notebooks, as well as created linked services to support the flow of data through the pipeline.
- Azure Databricks: I made three notebooks to house pySpark scripts to mount the storage containers from the data lake and transformed data from the Bronze to Silver layer and Silver to Gold layer.
- Azure Synapse Analytics: I utilized a stored procedure to load the Gold layer data from the data lake to a Serverless SQL Database instance.
- Azure Entra ID (formerly known as Azure Active Directory): I created and assigned permissions to a security group to abide by data governance best practices and ensure data can only be accessed by those within the group.

Power BI:

- 
- I connected Azure Data Factory, Azure Databricks, and Synapse Analytics to this Git repository for audit records and to have a centralized location to run processes from.
- I created three notebooks in Azure Databricks: One to mount the storage containers, one to transform data from the bronze to silver layer, and one to transform data from the silver to gold layer.
-   The workspace loaded a copy of this repo 

