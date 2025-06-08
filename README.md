

# 🚀 End-to-End Data Engineering & Analytics Project (Medallion Architecture)

## 📌 Project Overview

This project demonstrates a complete data engineering and analytics pipeline using **Azure cloud services** and **Power BI**. The architecture follows the **Medallion Architecture (Bronze → Silver → Gold)** to process and analyze sales, logistics, and order delivery data.

---

## 🔧 Technologies & Tools Used

* **Data Sources**: GitHub CSV files, MySQL
* **Data Ingestion**: Azure Data Factory (ADF)
* **Data Lake**: Azure Data Lake Storage Gen2 (ADLS Gen2)
* **Data Processing**: Azure Databricks (PySpark)
* **Data Warehouse**: Azure Synapse Analytics
* **Dashboarding**: Power BI
* **Storage Format**: Parquet
* **Architecture Pattern**: Medallion Architecture

---

## 🧱 Architecture

```
Data Sources (GitHub / MySQL)
         ↓
   🔹 Bronze Layer (Raw Data) - ADLS Gen2
         ↓
   🔸 Silver Layer (Transformed/Cleaned) - ADLS Gen2
         ↓
   🟡 Gold Layer (Analytical/Filtered) - ADLS Gen2
         ↓
     Power BI Dashboard (Sales, Logistics, Delivery)
```

---

## 🛠️ Pipeline Workflow

### 1. **Data Ingestion (Bronze Layer)**

* Fetched data from **GitHub** and **MySQL**.
* Used **Azure Data Factory** to move raw data into the **Bronze Layer** in **ADLS Gen2**.
![image alt](https://github.com/kiwa-debug/Olist-full-Data-Engg-and-Analysis/blob/64d134c9ba6f77beba46b569f70815ea31914d56/Azure%20Homepage.png)

### 2. **Data Transformation (Silver Layer)**

* Used **Azure Databricks** with **PySpark** to:

  * Clean, filter, and join datasets.
  * Perform necessary business logic.
* Saved the transformed data in **Parquet** format in the **Silver Layer**.
![image alt](https://github.com/kiwa-debug/Olist-full-Data-Engg-and-Analysis/blob/64d134c9ba6f77beba46b569f70815ea31914d56/Azure%20Databricks.png)

### 3. **Data Modeling (Gold Layer)**

* Used **Azure Synapse Analytics** to:

  * Filter data further for reporting needs.
  * Create **External Tables** on Gold data using **Parquet** format.
![image alt](https://github.com/kiwa-debug/Olist-full-Data-Engg-and-Analysis/blob/64d134c9ba6f77beba46b569f70815ea31914d56/DataSet%20list.png)
![image alt](https://github.com/kiwa-debug/Olist-full-Data-Engg-and-Analysis/blob/64d134c9ba6f77beba46b569f70815ea31914d56/Parquet%20Format.png)

### 4. **Data Visualization**

* Connected **Power BI** to the **Gold Layer**.
* Created dashboards analyzing:

  * **Sales Performance**
![image alt](https://github.com/kiwa-debug/Olist-full-Data-Engg-and-Analysis/blob/871cad9551683a3005386b03de4e5ee4b5b18f4d/Sales.png)
  * **Logistics Operations**
![image alt](https://github.com/kiwa-debug/Olist-full-Data-Engg-and-Analysis/blob/871cad9551683a3005386b03de4e5ee4b5b18f4d/Logistics.png)
  * **Order Delivery Status**
![image alt](https://github.com/kiwa-debug/Olist-full-Data-Engg-and-Analysis/blob/871cad9551683a3005386b03de4e5ee4b5b18f4d/Quality.png)

---

## 📊 Dashboard Highlights

* **Sales Trends by Region and Product**
* **Logistics Efficiency Analysis**
* **On-Time Delivery vs Delays**
* **Order Fulfillment Pipeline**

---

---

## 📈 Outcome

This project provides a robust and scalable solution for processing raw data from multiple sources, transforming it using Spark, and delivering actionable insights through dashboards — all following best practices in **modern data architecture**.

---

