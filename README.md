# Jing You - Data Engineering Portfolio

🌐 **Live Site**: [jingyou-data.github.io](https://jingyou-data.github.io)

## About This Site

A professional portfolio showcasing my work in **data engineering, analytics engineering, and modern ELT pipelines**.  
This site highlights end‑to‑end projects built with **SQLMesh, dbt, Airflow, Prefect, Snowflake, DuckDB, Power BI**, and other components of the modern data stack.

My focus is building **scalable, automated, and business‑impactful data systems**.

---

## Tech Stack

- **Modern Data Stack**: SQLMesh, dbt, Airflow, Prefect  
- **Data Warehousing**: Snowflake  
- **Lakehouse / Engines**: DuckDB, Databricks, Delta Lake  
- **Programming**: Python (Polars, Pandas), SQL  
- **APIs & Pipelines**: REST APIs, multi‑source ingestion, CI/CD  
- **BI & Analytics**: Power BI, DAX, Metabase  
- **DevOps**: GitHub Actions, Docker  
- **Hosting**: GitHub Pages (Markdown + Jekyll)

---

## Projects Featured

### ⭐ 1. MidTenn Lend Map — Small Business Lending Intelligence Platform  
**SQLMesh · Prefect · DuckDB · Snowflake · Power BI · 5 Public APIs**

End‑to‑end data engineering platform designed for **community banks in Middle Tennessee**, transforming public financial data into actionable lending intelligence.

- Multi‑source ingestion across **SBA, FDIC, CFPB, FRED, Census**  
- **Medallion architecture** (Bronze → Silver → Gold)  
- **19 SQLMesh models** orchestrated with Prefect  
- **2,300+ loan records** + **52,000+ complaint records** processed  
- **Geospatial insights** identifying underserved lending opportunities  
- Dual serving layers:  
  - Snowflake + Power BI (executive dashboards)  
  - PostgreSQL + Metabase (operational monitoring)

🔗 GitHub Repo: *[Add your link]*

---

### ⭐ 2. NPPES Healthcare Provider Pipeline — 8.85M Records  
**dbt · Snowflake · Airflow · Power BI**

A large‑scale ELT pipeline processing **8.85 million CMS provider records (9.9GB)** with automated testing and CI/CD.

- dbt models across staging → intermediate → marts  
- **16+ automated dbt tests**  
- Schema‑change detection + GitHub Actions CI/CD  
- Power BI semantic model + DAX measures  
- Familiarity with federal healthcare data governance

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
