# Azure-Data-Engineering-Project
Azure End-to-End Data Engineering Project 🌟
-
![Architecture Diagram](https://github.com/user-attachments/assets/47abf7e7-4b7a-4fb5-b824-06e1bb294220)

This project demonstrates a comprehensive Azure Data Engineering workflow using multiple Azure resources to process and analyze an e-commerce dataset. The dataset consists of 8 files containing details about customers, payments, orders, and other key information. Below is an in-depth description of the project architecture, process, and technologies used.

Dataset Overview 📊
The dataset used in this project is an e-commerce dataset, containing:
  - Customer details
  - Payment transactions
  - Order information
  - Other supporting data
  -This dataset is stored in multiple sources, including SQL, MongoDB, and HTTP (GitHub). It offers a realistic and complex scenario for data engineering.
![HRhd2Y0](https://github.com/user-attachments/assets/5602eb52-3824-4463-9101-3afda594ba83)


Azure Resources Utilized 💡
  - Azure Data Factory (ADF): For data ingestion and pipeline orchestration.
  - Azure Data Lake Storage Gen2 (ADLS Gen2): For storing raw, cleaned, and transformed data in Bronze, Silver, and Gold layers.
  - Azure Databricks: For data transformation, cleaning, and integration of datasets.
  - Azure Synapse Analytics: For querying, creating views, and further analysis.
  - Files.io Web: A source for SQL and MongoDB data.
  - HTTP Data Source (GitHub): Additional data source to simulate diverse data inputs.
![Screenshot (9)](https://github.com/user-attachments/assets/3082770f-da27-4e50-ba11-8c3667791b90)


Project Workflow 🔄

1. Data Ingestion (Bronze Layer)
  - The first step involves extracting raw data from various sources:
  - Files.io Web:
  - SQL database containing structured data.
  - MongoDB database containing semi-structured data.
  - Data manually uploaded for use as a source.
  - HTTP (GitHub):
  - Used as an additional source of data for variety.
  - Process in Azure Data Factory (ADF):
  - Created dynamic pipelines to extract data using Lookup, ForEach, and Copy Activities.
  - Data from SQL and HTTP sources was ingested and stored in the Bronze Layer of Azure Data Lake Storage Gen2 (ADLS Gen2) in its raw form.
![Screenshot (15)](https://github.com/user-attachments/assets/4f2f8dca-f82a-4077-8022-772ed221802d)
![Screenshot (4)](https://github.com/user-attachments/assets/56e7d573-6a2c-4064-ac5c-0bd538a6524f)


2. Data Transformation (Silver Layer)
  - Data transformation and cleaning were carried out in Azure Databricks. This included:
  - Configurations for ADLS Gen2 Access: Set up configurations to read raw data from the Bronze Layer.
  - MongoDB Integration: Read data from MongoDB to introduce complexity and simulate real-world data engineering.
  - Data Transformation Steps:

Cleaning:
  - Removed duplicate rows and columns.
  - Standardized formats across datasets.

Merging:
  - Joined multiple tables using specific keys.

Combined SQL and MongoDB datasets.
Output:
  - A final, cleaned, and enriched dataset was generated.
Stored the processed data in the Silver Layer of ADLS Gen2 in Parquet format.
![Screenshot (10)](https://github.com/user-attachments/assets/10e000c8-f38f-4f80-8441-db3d45aa4b1b)
![Screenshot (12)](https://github.com/user-attachments/assets/aa56a607-8a7c-4709-bc27-cb35983fba70)
![Screenshot (13)](https://github.com/user-attachments/assets/1947f601-6287-4c5f-9755-5a0497d9ccbc)


3. Data Analysis (Gold Layer)

  - The cleaned and transformed data from the Silver Layer was loaded into Azure Synapse Analytics for further analysis.
  - Process in Synapse Analytics:
  - Loaded data into Synapse for SQL-based querying.
  - Created views to summarize and analyze the dataset.
  - These views provided insights and were stored in the Gold Layer of ADLS Gen2 for downstream consumption.
![Screenshot (6)](https://github.com/user-attachments/assets/657b3815-50b0-4e10-a1be-4cfdef0ba505)
![Screenshot (7)](https://github.com/user-attachments/assets/a47d77a6-96b8-4bc9-9b28-7743e98c498f)



4. Visualization 
  - While the visualization was not the primary focus, initial efforts were made to use tools like Power BI to visualize the data. Future improvements could include:
Detailed dashboards.
Integration with Tableau or Power BI for real-time reporting.
Project Architecture 🏗️

Key Features and Highlights ✨

  - Dynamic Pipelines:
  - Used dynamic configurations in ADF to handle multiple data sources efficiently.
  - Real-World Complexity:
  - Combined data from SQL, MongoDB, and HTTP sources.

Layered Data Architecture:
  - Raw data stored in Bronze.
  - Cleaned and transformed data stored in Silver.
  - Aggregated and analyzed data stored in Gold.

Efficient Data Processing:
Used Azure Databricks for heavy transformations and cleaning.

SQL Analysis:
Performed in Synapse Analytics with views for insights.

Technologies Used 🛠️
  - Azure Data Factory: Dynamic pipelines for data ingestion.
  - Azure Data Lake Storage Gen2: Storage layers for the data lifecycle.
  - Azure Databricks: Data cleaning, transformation, and integration.
  - Azure Synapse Analytics: SQL-based querying and analysis.
  - MongoDB: Semi-structured data source.
  - HTTP (GitHub): Additional data source.
  - Power BI: For initial visualization.


Future Enhancements 🚀
  - Advanced Visualizations: Create interactive dashboards using Power BI and Tableau.
  - Data Enrichment: Introduce additional datasets for more insights.


Contact 📧

For any queries or feedback, feel free to reach out at chiragbhutada@gmail.com

