# Azure Data Ingestion & Integration Framework

## 🚀 Project Overview

This project is a **framework to handle current and future data ingestion from SQL, FTP, REST APIs** into **Azure Data Lake Storage (ADLS)** using **Azure Data Factory (ADF)**.

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

---

## 🙌 Author

Bharath — Azure Data Engineering Project


