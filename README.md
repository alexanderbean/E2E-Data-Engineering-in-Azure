# End-to-End ETL Pipeline in Microsoft Azure - (e2e-de-azure)

This is my first complete end-to-end data engineering project. In this project, I created an end-to-end ETL pipeline starting from an on-prem SQL Server Database, moving into the Azure cloud, and ending with a Power BI dashboard/report.

My goals for this project were:
- To gather a general understanding of what makes a data engineering pipeline,
- To gain hands-on experience with the Azure cloud platform and offered services, and
- To produce a functional and stable end product to showcase on GitHub and my resume.

For a data source, I used one of Microsoft's sample lightweight datasets: [AdventureWorksLT2022](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorksLT2022.bak)

![azurediagram](https://github.com/user-attachments/assets/df2c0dc6-49de-412f-b4b9-f0aa63f74b7f)

# Project Steps

**On-Prem SQL Server Database:**
- Before starting on the cloud, I installed SQL Server Express to host the local server and set up SQL Server Management Studio.
- I also downloaded the Java Runtime Environment (JRE) to support the Parquet format.

**Github:**
- I created this repository to track the progression of the project.
- When Azure Data Factory, Azure Databricks, and Azure Synapse Analytics were created: I completed Git configuration within the instances so any changes or publishes were pushed to a branch for easy audit/documentation.

**Microsoft Azure:**
- Once in Azure, I established the resource group and all necessary Azure resources within the group.
- Azure Data Lake Storage Gen2: I created the storage containers for the Bronze, Silver, and Gold layers.
- Azure Key Vault: I assigned secrets to the login and password of the local SQL database to be used in linked services in Azure Data Factory.
- Azure Data Factory (ADF): I engineered the pipelines to extract the data from the on-prem database and to execute the Databricks notebooks, as well as created linked services to support the flow of data through the pipeline.
- Azure Databricks: I made three notebooks to house pySpark scripts to mount the storage containers from the data lake and transformed data from the Bronze to Silver layer and Silver to Gold layer.
- Azure Synapse Analytics: I utilized a stored procedure to load the Gold layer data from the data lake to a Serverless SQL Database instance.
- Azure Entra ID (formerly known as Azure Active Directory): I created and assigned permissions to a security group to abide by data governance best practices and ensure data can only be accessed by those within the group.

**Power BI Desktop:**
- I loaded the Gold layer database from Azure Synapse Analytics to Power BI Desktop and reviewed/revised the connections between tables.
- I visualized a few metrics for the number of customers, number of sales, and total revenue.
- Additionally, I created slicers for state/province and products, so a user can filter by those fields to see the above metrics.

