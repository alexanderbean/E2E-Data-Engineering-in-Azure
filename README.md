# End-to-End ETL Pipeline in Microsoft Azure - (e2e-de-azure)

This is my first complete data engineering project and my first non-academic project. In this project, I created an end-to-end ETL pipeline starting from an on-prem SQL Server Database, moving into the Azure cloud, and ending with a Power BI dashboard/report.

My goals for this project were:
- To gather a general understanding of what makes a data engineering pipeline,
- To gain hands-on experience with the Azure cloud platform and offered services, and
- To produce a functional and stable end product to showcase on GitHub and my resume.

The dataset used was the Microsoft lightweight AdventureWorksLT2022 set: https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver16&tabs=ssms

In this project, I used:

- Azure Gen2 Data Lake Storage
- Azure Data Factory
- Azure Databricks
- On-prem SQL Server Database
- SQL Server Management Studio (SSMS)
- Azure Synapse Analytics
- Serverless Azure SQL Database
- Azure Entra ID (prev. known as Azure Active Directory)
- Azure Key Vault
- Power BI Desktop

These are the major steps I took in creating this end-to-end project:

- 
- I connected Azure Data Factory, Azure Databricks, and Synapse Analytics to this Git repository for audit records and to have a centralized location to run processes from.
- I created three notebooks in Azure Databricks: One to mount the storage containers, one to transform data from the bronze to silver layer, and one to transform data from the silver to gold layer.
-   The workspace loaded a copy of this repo 

