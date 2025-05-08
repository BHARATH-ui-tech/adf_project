# Azure Data Ingestion & Integration Framework

## 🚀 Project Overview

This project provides a scalable and reusable framework to handle current and future data ingestion from SQL databases, FTP sources, and REST APIs into Azure Data Lake Storage (ADLS) using Azure Data Factory (ADF).

---

## 📁 Structure
├── datasets/ → All dataset JSON files used in pipelines
├── linkedservices/ → Linked services to connect to SQL, ADLS, REST
├── pipelines/ → Main ADF pipelines (dynamic framework)
└── README.md → Project documentation


---

## 🔧 What This Project Does

- Uses **config table** to handle multiple source types (SQL, FTP, REST)
- Ingests data dynamically using one master pipeline
- Sends data into **Azure Data Lake** in correct folder format
- Uses **Switch-Case logic**, **parameters**, and **ForEach loop**
- Supports easy **extension for future sources**

---

## 🛠️ Technologies Used

- Azure Data Factory (ADF)
- Azure SQL Database
- Azure Data Lake Storage (Gen2)
- REST APIs
- JSON, CSV, Avro, Parquet file handling

---

## 🧪 Example Pipelines

- `pl_ingest`: Main orchestrator pipeline
- `sql_2_adls`: SQL-to-ADLS child pipeline
- `ftp_2_adls`: FTP-to-ADLS child pipeline
- `rest_2_adls`: REST API ingestion pipeline

---

✅ Notes

This project is a modular and scalable Azure Data Factory (ADF) implementation designed to handle diverse data ingestion pipelines including SQL databases, REST APIs, and FTP sources. The design promotes reusability, parameterization, and centralized control through metadata-driven configuration.

📌 Key Highlights:

 * Dynamic Pipelines: All pipelines are parameterized to support dynamic data movement based on configuration tables.

 * Metadata-Driven Design: Uses a centralized SQL configuration table to determine source type, queries, output format, directory path, and filenames dynamically.

 * Reusable Components: Pipelines and datasets are built to be reusable across multiple ingestion scenarios (SQL, REST, FTP).

  *  Structured Repo: Clean separation of components into:

        pipelines/: Contains the main and child pipelines.

        datasets/: Source and sink datasets used in the pipelines.

        linkedservices/: Secure connections to Azure services (SQL, ADLS, REST APIs).

   * Error Handling & Auditing: Built-in variables to pass and capture errors, file-level information, and control parameters for better logging and monitoring (to be enhanced in future iterations).

   * Future-Proof Design: Easily extendable to support more source types like SFTP, blob storage, etc.

💡 Best Use Case:

This framework is ideal for teams or data engineers who want to automate and control data movement from heterogeneous sources to a unified data lake or warehouse.

---

## 🙌 Author

Bharath — Azure Data Engineering Project
