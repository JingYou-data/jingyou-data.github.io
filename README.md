---
layout: default
title: Home
---
# 👋 Hi, I'm Jing You  
**Data Engineering & Analytics Engineering | Microsoft Fabric | Power BI | Python | SQL**
I build scalable data systems that turn raw information into actionable insights.  
My background blends business operations, customer understanding, and technical engineering — giving me a unique edge in solving real-world data problems.

---

# ⚡ Core Skills

### **Data Engineering**
- ETL / ELT pipeline development  
- REST API integration  
- Data modeling & transformation  
- Data validation & quality assurance  
- Batch processing & automation  

### **Technologies**
- **Python:** Pandas, Polars, Requests  
- **SQL:** PostgreSQL, DuckDB  
- **Cloud:** AWS (S3, Lambda)  
- **Tools:** Docker, Git, VS Code Dev Containers  
- **Data Formats:** JSON, Parquet, CSV  

### **Currently Learning**
- dbt  
- Apache Airflow  
- Microsoft Fabric  

---

# 💼 Featured Projects

---

## **📌 NPPES Medical Provider Data Pipeline**
**Tech Stack:** Python, AWS S3, PostgreSQL, Docker  
A full batch ETL pipeline processing **8.7 million** medical provider records.

### **Highlights**
- Automated ingestion using AWS Lambda  
- Efficient processing of multi-million–row datasets  
- Structured logging for traceability  
- End-to-end containerized workflow  

👉 [View Project →](https://github.com/JingYou-data/NPPES)

---

## **⭐ MidTenn Lend Map — Small Business Lending Intelligence Platform**
**Tech Stack:** SQLMesh · Prefect · DuckDB · Snowflake · Power BI · Metabase · 5 Public APIs  
End-to-end data engineering platform designed for community banks in Middle Tennessee.

### **Engineering Highlights**
- Multi-source ingestion across SBA, FDIC, CFPB, FRED, and Census APIs
- Medallion architecture (Bronze → Silver → Gold)
- 19 SQLMesh models orchestrated with Prefect
- 2,300+ loan records + 52,000+ complaint records processed
- Dual serving layers: Snowflake + Power BI (executive dashboards) and PostgreSQL + Metabase (operational monitoring)

### **Power BI Work**
- Executive dashboard built on Snowflake
- DAX measures for loan performance, complaint trends, and risk scoring
- Geospatial visuals identifying underserved lending regions
- Semantic model aligned with business entities (Loans, Banks, Complaints, Regions)

👉 [View Project →](https://github.com/JingYou-data/MidTenn_Lend_Map)

---

## **📌 Weather Data Integration Pipeline**
**Tech Stack:** Python, REST API, Pandas, PostgreSQL, DuckDB, Docker  
A multi-source data pipeline combining real-time weather data with station metadata.

### **Core Features**
```python
merged = weather_df.merge(stations_df, on='city', how='inner')
merged.to_parquet('weather_clean.parquet')
# Data Validation with DuckDB
con.execute("""
    SELECT COUNT(*) as null_count
    FROM weather WHERE temperature_f IS NULL
""")
```

### **Project Highlights**
- RESTful API integration with authentication & rate limiting  
- Data cleaning & merging using Pandas (Inner Join)  
- 6-layer data validation using DuckDB  
- Parquet columnar storage → **10× faster queries**  
- Fully containerized with Docker + Dev Container  

### **Business Impact**
Enables analysis of weather-driven business patterns:
- Customer traffic changes on rainy days  
- Outdoor seating optimization  
- Staffing adjustments based on forecasts  

---

# 🧠 How I Think About Data Engineering

### **Systems Over Scripts**
I design pipelines that are:
- Maintainable  
- Scalable  
- Observable  
- Documented  

### **Data Quality First**
Bad data = bad decisions.  
I prioritize:
- Validation  
- Schema consistency  
- Reproducibility  

### **Business-Aware Engineering**
My hospitality and operations background helps me:
- Understand real business workflows  
- Identify high-impact opportunities  
- Communicate clearly with non-technical teams  

---

# 📬 Contact
**Open to Data Engineer / Analytics Engineer / BI roles (Nashville or Remote)**
- 📧 Email: **jingliuyou@gmail.com**  
- 📍 Nolensville, Tennessee
