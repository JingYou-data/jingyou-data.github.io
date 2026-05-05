# Jing You - Data Engineering Portfolio

🌐 **Live Site**: [jingyou-data.github.io](https://jingyou-data.github.io)

## About This Site

A professional portfolio showcasing my work in **data engineering, analytics engineering, and business intelligence**.  
This site highlights end‑to‑end ELT pipelines, semantic modeling, and modern data stack projects built with:

- SQLMesh  
- dbt  
- Airflow  
- Prefect  
- Snowflake  
- DuckDB  
- Power BI  
- Python (Polars, Pandas)

My focus is building **scalable, automated, and business‑impactful data systems** that transform raw data into reliable insights.

---

## Tech Stack

- **Modern Data Stack**: SQLMesh, dbt, Airflow, Prefect  
- **Data Warehousing**: Snowflake  
- **Lakehouse / Engines**: DuckDB, Databricks, Delta Lake  
- **Programming**: Python (Polars, Pandas), SQL  
- **APIs & Pipelines**: REST APIs, multi‑source ingestion, CI/CD  
- **BI & Analytics**: Power BI, DAX, Semantic Modeling, Metabase, Geospatial Analysis  
- **DevOps**: GitHub Actions, Docker  
- **Hosting**: GitHub Pages (Markdown + Jekyll)

---

## Projects Featured

### ⭐ 1. MidTenn Lend Map — Small Business Lending Intelligence Platform  
**SQLMesh · Prefect · DuckDB · Snowflake · Power BI · Metabase · 5 Public APIs**

End‑to‑end data engineering platform designed for community banks in Middle Tennessee.

**Engineering Highlights**
- Multi‑source ingestion across **SBA, FDIC, CFPB, FRED, Census**  
- **Medallion architecture** (Bronze → Silver → Gold)  
- **19 SQLMesh models** orchestrated with Prefect  
- **2,300+ loan records** + **52,000+ complaint records** processed  
- Dual serving layers:  
  - Snowflake + Power BI (executive dashboards)  
  - PostgreSQL + Metabase (operational monitoring)

**Power BI Work**
- Executive dashboard built on Snowflake  
- DAX measures for loan performance, complaint trends, and risk scoring  
- Geospatial visuals identifying underserved lending regions  
- Semantic model aligned with business entities (Loans, Banks, Complaints, Regions)

🔗 GitHub Repo: *[Add your link]*

---

### ⭐ 2. NPPES Healthcare Provider Pipeline — 8.85M Records  
**dbt · Snowflake · Airflow · Power BI**

Large‑scale ELT pipeline processing **8.85 million CMS provider records (9.9GB)** with automated testing and CI/CD.

**Engineering Highlights**
- dbt models across staging → intermediate → marts  
- **16+ automated dbt tests**  
- Schema‑change detection + GitHub Actions CI/CD  
- Airflow DAG for scheduled ingestion + transformation  
- Data quality and documentation integrated into workflow

**Power BI Work**
- Provider segmentation dashboard  
- DAX measures for provider density, specialty distribution, and geographic coverage  
- Snowflake‑based semantic model  
- Data quality indicators surfaced in BI layer

🔗 GitHub Repo: *[Add your link]*

---

### ⭐ 3. Additional Engineering Work  
**Python · Polars · FastAPI · PostgreSQL · Databricks · Kafka**

- Designed relational databases + REST APIs with FastAPI  
- Built data transformations using Polars/Pandas  
- Worked with Databricks + Delta Lake  
- Implemented streaming patterns (Kafka/pub‑sub)  
- Applied Git/GitHub for version control, CI/CD, documentation

---

## Local Development

```bash
git clone https://github.com/jingyou-data/jingyou-data.github.io.git

# Navigate to directory
cd jingyou-data.github.io

# View locally (if using Jekyll)
bundle exec jekyll serve
