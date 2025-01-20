# Azure Data Engineering Project: NYC Taxi Data Pipeline

### Project Overview

This project demonstrates the implementation of an end-to-end **Azure Data Engineering** pipeline using the **Medallion Architecture** (Bronze, Silver, Gold) to transform raw data into actionable insights. The project focuses on ingesting, transforming, and storing **NYC Taxi data** from an external web-hosted API using **Azure Data Factory (ADF)**, **Azure Databricks**, and **Delta Tables**.

## Tools and Technologies
- **Azure Data Factory (ADF)**
- **Azure Databricks (PySpark)**
- **Azure Data Lake Gen2**
- **Microsoft Entra ID**
- **Python**
- **SQL**
  
## Architecture Overview
![image](https://github.com/Swaleen277/ADE-NYC-Taxi-Project/blob/main/Images/Data%20Architecture.jpg?raw=true)

### Project Workflow
Extracted NYC taxi data from an external web-hosted API using **Azure Data Factory (ADF)** and Transformed the data using **Azure Databricks** and on top of that built **Delta Tables**.

![image](https://github.com/Swaleen277/ADE-NYC-Taxi-Project/blob/main/Images/Resource%20Group.JPG?raw=true)

#### 🔹 **Data Ingestion with Azure Data Factory (ADF)**

- **Source**: Ingested **NYC Taxi data** from an external web-hosted **API**.
- **Pipeline**: Created dynamic pipelines in **ADF** to ingest the data into **Azure Data Lake Gen2**.
- **Hierarchical Namespace**: Enabled for efficient data organization using directories and subdirectories, improving performance and management of large datasets.
- **Storage**: Data was stored in the **Bronze Layer** for further processing and transformation.
  
  ![image](https://github.com/Swaleen277/ADE-NYC-Taxi-Project/blob/main/Images/ADF_Pipeline1.JPG?raw=true)
  ![image](https://github.com/Swaleen277/ADE-NYC-Taxi-Project/blob/main/Images/ADF_Pipeline2.JPG?raw=true)
 
#### 🔹 **Data Transformation with Azure Databricks & PySpark**

- **Transformation**: Performed data transformation in **Azure Databricks**, leveraging **PySpark** for processing.
- **Connection**: Established a secure connection between **Azure Data Lake Gen2** and **Databricks** using **Microsoft Entra ID** to enable seamless data transformation.
  
  ![image](https://github.com/Swaleen277/ADE-NYC-Taxi-Project/blob/main/Images/silver_notebook.JPG?raw=true)
  ![image](https://github.com/Swaleen277/ADE-NYC-Taxi-Project/blob/main/Images/gold_notebook.JPG?raw=true)


#### 🔹 **Storing Transformed Data in Delta Tables**

- **Delta Tables**: Transformed data was saved in **Delta Tables** within the **Gold Layer**.
- **ACID Compliance**: Delta Tables ensure **ACID compliance**, improving data reliability and consistency.
- **Version Control**: Used the **Delta Table format** for version control, allowing historical changes to be tracked and easily accessible.

---

### Key Learnings

- Built scalable, efficient, and secure data pipelines from ingestion to transformation.
- Mastered the usage of **Azure Data Factory**, **Azure Databricks**, **Delta Tables**, and **PySpark** for building robust data workflows.
  
