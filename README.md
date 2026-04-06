# Azure Data Factory Project

## Project Overview
This project demonstrates a robust data engineering pipeline using **Azure Data Factory (ADF)**. It implements a **Medallion Architecture**, ensuring data moves seamlessly from raw sources to refined, high-quality datasets ready for analytics and reporting. The pipeline integrates multiple data sources, handles incremental updates, and notifies stakeholders if issues occur.

---

## Architecture
The data flow follows a **Medallion Architecture** with **Bronze**, **Silver**, and **Gold** layers:

### Bronze Layer (Raw Data)
- Data is ingested from on-premises SQL servers, APIs, and GitHub repositories.
- Stores raw, unprocessed data in a **Data Lake**.

### Silver Layer (Cleaned & Incremental Data)
- Incremental transformations are applied to **cleanse and standardize** the data.
- Pipelines are designed to handle **large datasets efficiently**.

### Gold Layer (Aggregated & Analytics-Ready)
- Final transformations produce **high-quality, business-ready datasets**.
- Data is ready for **analytics, reporting, or downstream applications**.

### Architecture Diagram
![Architecture](https://github.com/MarkMarei/Azure-Data-Factory-Project/blob/258748b7c87897f388820b22dbb3ce22133e3fdd/Architecture.png)

---

## Parent Pipeline
The **parent pipeline** orchestrates multiple child pipelines, including:

- **Incremental Load Pipelines** – Load to Bronze layer with new or modified records.
- **API Ingestion Pipeline** – Fetches data from external APIs.
- **On-Prem File Upload** – Moves on-premises files to the cloud for processing.

This ensures a **streamlined and reliable ETL process**.

### Example Visualization
![Parent Pipeline Execution](https://github.com/MarkMarei/Azure-Data-Factory-Project/blob/830bf9eef22bcc3cd55c3c72f3e56c59fbd5a07f/ParentPipeline.png)

### Incremental Load Pipeline
![Parent Pipeline Execution](https://github.com/MarkMarei/Azure-Data-Factory-Project/blob/830bf9eef22bcc3cd55c3c72f3e56c59fbd5a07f/Incremental.png)

---

## Error Notifications
Automated **email notifications** are sent if any pipeline encounters an error, allowing quick identification and resolution without manual monitoring.

### Sample Error Email
![Error Notification](https://github.com/MarkMarei/Azure-Data-Factory-Project/blob/830bf9eef22bcc3cd55c3c72f3e56c59fbd5a07f/EmailContent.png)

---

## Transformations
Data transformations are performed in multiple stages:

- **Bronze Layer**: Getting the raw data.
- **Silver Layer**: Standardization and cleansing.
- **Gold Layer**: Aggregations, joins, and business logic applied.

### Example Transformation Logic
![Transformation Example](https://github.com/MarkMarei/Azure-Data-Factory-Project/blob/830bf9eef22bcc3cd55c3c72f3e56c59fbd5a07f/Transformations.png)

---

## Conclusion
This project demonstrates a **fully managed ETL workflow** in Azure, following Medallion Architecture principles. It ensures:

- Reliable ingestion from multiple sources.
- Incremental updates to optimize processing.
- Error monitoring and notifications.
- High-quality, analytics-ready datasets.
