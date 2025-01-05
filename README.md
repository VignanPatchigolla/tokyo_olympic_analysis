# 🏅 Tokyo Olympics Data

## 🌟 Overview

This project processes and transforms **Tokyo Olympics** data from multiple CSV sources into a structured and aggregated format. The workflow includes data ingestion, transformations, and storage in different layers (Bronze, Silver, Gold) within Azure Data Lake Storage (ADLS). The final data is utilized for analytics in **Synapse Analytical Workspace**.

## 📚 Data Sources

- **Athletes.csv**: Details of athletes participating in the Olympics.
- **Teams.csv**: Information about participating teams.
- **Coaches.csv**: List of coaches.
- **EntriesGender.csv**: Gender-based entries.
- **Medals.csv**: Medal tally data.

## 🛠️ Workflow

1. **📥 Data Ingestion**:
   - Data is fetched from an API and ingested into the **Bronze** container in ADLS using Azure Data Factory (ADF).

2. **🔄 Data Transformation**:
   - Validations and transformations are performed on the raw data, and the processed data is stored in the **Silver** container.

3. **📊 Data Aggregation**:
   - Data is aggregated using SQL queries to create analytics-ready datasets, which are stored in the **Gold** container.

4. **🔎 Analytics**:
   - Sample insights and dashboards are created in the **Synapse Analytical Workspace**.

## 🔧 Technologies Used

- 🗄️ **Azure Data Lake Storage (ADLS)**: For storing raw, transformed, and aggregated data.
- 🔄 **Azure Data Factory (ADF)**: For orchestrating data ingestion and transformation pipelines.
- 🧱 **Databricks**: For performing transformations and advanced data processing.
- 📜 **SQL Database**: Used for schema validation and aggregations.
- 🛠️ **Synapse Analytics**: For building analytical workspaces and sample dashboards.

## 📂 Repository Structure
```plain.text
tokyo-Olympics-Data-Project/ 
├── credential/           # Contains synapse credential files and configurations 
├── database/             # Contains Synapse databases  
├── databricks/           # Databricks notebooks for data processing 
├── dataset/              # Sample datasets for testing 
├── datasets/             # Raw datasets used in the project 
├── factory/              # ADF pipelines for data ingestion 
├── integrationRuntime/   # Integration runtime configurations for ADF 
├── linkedService/        # Linked service definitions for ADF 
├── pipeline/             # Pipelines for data processing 
├── sqlscript/            # SQL scripts for data aggregation
├── architecture/         # Architecture diagram for the project
└── README.md             # Project overview (this file)
```

## 🚀 How to Use

1. **🔑 Setup Credentials**:
   - Store API and ADLS credentials in **Azure Key Vault** or the `credential` directory.

2. **🔄 Run Pipelines**:
   - Use ADF pipelines in the `factory` directory to ingest data into the Bronze layer.

3. **📂 Process Data**:
   - Use Databricks notebooks in the `databricks` directory to transform data into the Silver and Gold layers.

4. **📊 Analyze Data**:
   - Use the Synapse Analytical Workspace to create visualizations and insights from the Gold data.

## 🌟 Highlights
- Automated and efficient data pipeline design.
- Clean and modular folder structure for ease of collaboration.
- Utilization of modern cloud tools like **Azure Data Factory**, **Databricks**, and **Synapse Analytics**.

## 🛠️ Future Enhancements
- 🤖 Integration of real-time data processing.
- ⚡ Adding more detailed dashboards in Synapse Analytics.
- 🗂️ Partitioning and optimization of Gold-layer data for faster queries.

## 📬 Contact
For any queries, feel free to reach out to the repository maintainer at **[your-email@example.com](vignanpatchigolla5.com)**.

