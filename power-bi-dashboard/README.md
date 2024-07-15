# Power BI - (pbi-e2e-de)

This results from the ETL pipeline and offers an interactive reporting and analytics experience.

Power BI Desktop loads the data from the "gold_db" table created in Azure Synapse Analytics.

Why use the Azure Synapse database as the source VS the Gold container in the Data Lake?
- It's an established best practice to use a database as the serving layer for Power BI reporting.
- The Synapse database offers greater scalability and easier maintenance than reporting from the Data Lake.

The Desktop version is included in this folder to download and experiment with the visualizations. The dashboard is also published to the Power BI Service (and Microsoft Fabric) but cannot be accessed by users outside my organization.

![pbi-dash](https://github.com/user-attachments/assets/571f0eb7-e412-4fb0-a0ef-22acb5b2f13e)
